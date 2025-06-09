# DCGS – Discrete Cadastral Grid System

⚠️ *Working title – this is a conceptual and research-stage repository. The project name may change as implementation evolves.*

## 📍 Overview

DCGS is a **Discrete Global Grid System (DGGS)** specifically designed for **terrestrial cadastral mapping**. Unlike general-purpose DGGSs, DCGS prioritizes cadastral accuracy, equal-area indexing, GNSS compatibility, and blockchain integration.

This project is based on the academic article:

> **"Designing a parallelogram Discrete Global Grid System for terrestrial cadastral mapping"**  
> *Israel Nunes da Silva, Elcio H. Shiguemori, Gabriel Dietzsch*  
> *(Instituto Tecnológico de Aeronáutica – ITA, Instituto de Estudos Avançados – IEAv)*

---

## 🌎 Motivation

Cadastral systems require high-resolution and legally reliable mapping. Traditional GIS platforms struggle to provide scalable, interoperable frameworks that integrate blockchain or GNSS with cadastral needs.  
DCGS addresses this by offering:
- Equal-area parallelogram-based cell structure  
- Sinusoidal projection over the ellipsoidal Earth model  
- Metric-based multiscale indexing  
- Centimeter-level compatibility with GNSS systems  
- Blockchain-ready cell encoding for immutable spatial records

---

## 🧱 Design Highlights

| **Design Criteria**         | **DCGS Solution**                                        |
|-----------------------------|-----------------------------------------------------------|
| Purpose-Oriented            | Matches cadastral scales with minimal distortion         |
| Equal-Area Cells            | Uses uniform area cells, even over an ellipsoid          |
| Multi-Scale Support         | 1-to-4 and 1-to-25 refinement hierarchy                  |
| GNSS Compatibility          | Aligns with WGS84 ellipsoid at centimeter resolution     |
| Simple Shape                | Uses parallelograms for computation and clarity          |
| Blockchain Integration      | Indexes designed for tokenization and traceability       |
| Geoprofessionals Usability  | Follows Cartesian logic familiar to geoinformation users |

---

## 🧩 Indexing Method

DCGS uses a hybrid indexing strategy:
- Quadrants (`NW`, `NE`, etc.) as primary level  
- 10 km × 10 km cells for Resolution 1  
- Hierarchical refinements:  
  - 1-to-4: `1`, `2`, `3`, `4`  
  - 1-to-25: `A1` to `E5`

Resolution levels span from 10 km down to 1 cm, supporting both rural parcels and detailed urban divisions.

---

## 🚧 Future Work

The following are planned for implementation:

- 🔧 Algorithm development (cell generation, coordinate conversion)  
- 💾 Binary codification and indexing optimization
- 🗺️ GIS integration modules and tools

---

## 📖 Reference

If you use or cite this project, please refer to the paper:

> **Silva, I. N., Shiguemori, E. H., Dietzsch, G.**  
> *Designing a parallelogram Discrete Global Grid System for terrestrial cadastral mapping*  
> [Publication info/link](http://mtc-m16c.sid.inpe.br/col/sid.inpe.br/mtc-m16c/2025/06.04.13.53/doc/thisInformationItemHomePage.html)

---

## 🛠️ License

MIT License

Copyright (c) 2025
Israel Nunes da Silva (ITA)  
Elcio Hideichi Shiguemori (IEAv)  
Gabriel Dietzsch (IEAv)

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 📬 Contact

For questions or collaboration opportunities:  
📧 israelnunes@ita.br  
✉️ [GitHub Issues](https://github.com/ICartCWB/DCGS/issues)
