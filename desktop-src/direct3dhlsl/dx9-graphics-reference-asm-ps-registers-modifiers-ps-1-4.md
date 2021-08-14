---
title: '\_ \_ modificateurs de Registre source PS 1 4 pour texld, texcrd'
description: Les instructions de texture de deux nuanceurs de pixels version 1 \_ 4, texld-PS \_ 1 \_ 4 et texcrd-PS, ont une syntaxe personnalisée.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 63a0cfd212767a0219af83d734d3562edacc84901098afcf77c786d8895f32d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512875"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>\_ \_ modificateurs de Registre source PS 1 4 pour texld, texcrd

Les instructions de texture de deux nuanceurs de pixels version 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) et [texcrd-PS](texcrd---ps.md), ont une syntaxe personnalisée. Ces instructions prennent en charge leur propre ensemble de modificateurs de Registre source, de sélecteurs de Registre source et de masques d’écriture de registre de destination, comme illustré ici.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Modificateurs de Registre source pour texld et texcrd

Ces modificateurs fournissent une fonctionnalité de division projective en divisant les valeurs x et y par les valeurs z ou w.



| Modificateurs de Registre source | Description                | Syntaxe       |
|---------------------------|----------------------------|--------------|
| \_DZ                      | Diviser les composants x, y par z | inscrire \_ DZ |
| \_db                      | Diviser les composants x, y par z | inscrire la base de référence \_ |
| \_DW                      | Diviser les composants x, y par w | inscrire la \_ DW |
| \_da                      | Diviser les composants x, y par w | inscrire \_ da |



 

### <a name="remarks"></a>Remarques

Le \_ \_ modificateur DZ ou DB effectue les opérations suivantes :


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



Le \_ \_ modificateur DW ou da effectue les opérations suivantes :


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




