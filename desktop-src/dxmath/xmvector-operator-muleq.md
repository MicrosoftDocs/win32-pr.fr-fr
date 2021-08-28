---
description: Opérateurs d’assignation de multiplication.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: opérateurs * =, opérateur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13280fd5da109012ac90ff55a778f8f5cd6a5b95
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627725"
---
# <a name="operator--operators"></a>Operator \* =, opérateurs

Opérateurs d’assignation de multiplication

### <a name="overload-list"></a>Liste de surcharge



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Opérateur</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR :: Operator * = (XMVECTOR&, float)</strong></a></td>
<td >Multiplie une <code>XMVECTOR</code> instance par une valeur à virgule flottante et retourne une référence à l’instance mise à jour. <br/> Le <code>operator *=</code> multiplie chaque composant de l’instance actuelle du <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par une valeur à virgule flottante spécifiée, en retournant une référence à l’instance actuelle mise à jour. <br/>
<blockquote>
[!Note]<br />
Cet opérateur est uniquement disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td ><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR :: Operator * = (XMVECTOR&, XMVECTOR)</strong></a></td>
<td >Multiplie une <code>XMVECTOR</code> instance par une deuxième instance, en retournant une référence à l’instance initiale mise à jour. <br/> Le <code>operator *=</code> multiplie chaque composant de l’instance actuelle du <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par le composant correspondant dans une deuxième instance spécifiée de <code>XMVECTOR</code> , en retournant une référence à l’instance initiale mise à jour. <br/>
<blockquote>
[!Note]<br />
Cet opérateur est uniquement disponible en C++.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[XMVECTOR, opérateurs](ovw-xmvector-operators.md)
</dt> <dt>

**Référence**
</dt> <dt>

[**Type de données XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 
