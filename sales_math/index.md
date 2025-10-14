---
layout: default
title: Sales Math
---

{% for formula in site.data.formulas %}
	{% include formula.html formula=formula %}
{% endfor %}


---
**Explanation**  
Margin is expressed as a decimal (e.g., 30% → 0.30).  This formula “grosses up” cost to the selling price, ensuring the margin is preserved.  

**Example:** Cost = $70, Margin = 0.30  

$$
\text{Price} = \frac{70}{1 - 0.30} = \frac{70}{0.70} = 100""")
$$

---
### Cost given Price and Margin
$$
\text{Cost} = \text{Price} \times (1 - \text{Margin})
$$

**Explanation**  
Rearranging the price formula allows cost to be derived from price and margin.  

**Example:** Price = $100, Margin = 0.30  

$$
\text{Cost} = 100 \times (1 - 0.30) = 70
$$

# Margin given Cost and Price
### Margin given Cost and Price
$$
\text{Margin} = \frac{\text{Price} - \text{Cost}}{\text{Price}}
$$

**Explanation**  
Margin is profit divided by price.  

**Example:** Price = $100, Cost = $70  
$$
st.latex(r"""\text{Margin} = \frac{100 - 70}{100} = 0.30 \; (30\%)""")
$$

# Discount given Cost and Price
### Discount given Cost and Price
$$
\text{Discount} = 1 - \frac{\text{Price}}{\text{List Price}}
$$

**Explanation**  
Discount is the percentage reduction from list price.  
(If you only have cost & net price, discount can be derived from the assumed list price.)  

**Example:** List Price = $120, Price = $100  
$$
\text{Discount} = 1 - \frac{100}{120} = 0.167 \; (16.7\%)
$$

# Margin given Distributor Discount and Customer Discount
### Margin with Distributor vs. Customer Discount
$$
\text{Distributor Margin} =
\frac{\text{Customer Price} - \text{Distributor Price}}{\text{Customer Price}}
$$

**Explanation**  
When both distributor and customer discounts apply, the distributor's margin is determined by the gap between the two net prices:  

- Distributor Price = List Price × (1 − Distributor Discount)  
- Customer Price = List Price × (1 − Customer Discount)  

**Example:**  
- List Price = $100  
- Distributor Discount = 40% → Distributor Price = $60  
- Customer Discount = 20% → Customer Price = $80  
$$
\text{Distributor Margin} = \frac{80 - 60}{80} = 0.25 \; (25\%)""")
$$


# Insert usage formulas
### Insert Usage per Part

# Core formula (real-valued)
$$
I_p \;=\; \frac{\dfrac{z}{z_i}}{T} \;=\; \frac{z}{z_i\,T}
$$


**Where:**  
- $I_p$ = inserts used per part (expected, real-valued)  
- $z$ = number of teeth (inserts mounted in cutter body)  
- $z_i$ = number of usable edges per insert  
- $T$ = tool life (parts per insert change)

**Interpretation:**  
- The formula yields the expected fraction of an insert consumed by a single part.  
- For planning a batch of $N$ parts, use `Inserts_consumed = (z/z_i) * (N/T)`.  
- Since inserts are discrete, round up to order:  

$$
\text{Inserts\_needed}(N) = \left\lceil \frac{z}{z_i} \cdot \frac{N}{T} \right\rceil
$$

# Worked numeric example (LaTeX)
$$
\begin{aligned}
z &= 6,\quad z_i = 2,\quad T = 100 \\
I_p &= \frac{6}{2\cdot 100} = 0.03\ \text{inserts/part} \\
\text{Inserts\_consumed}(1000) &= 0.03 \times 1000 = 30 \\
\text{Inserts\_needed}(1000) &= \left\lceil 30 \right\rceil = 30
\end{aligned}
$$