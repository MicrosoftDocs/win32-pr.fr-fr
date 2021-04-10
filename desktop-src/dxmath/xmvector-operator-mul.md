---
description: Opérateurs de multiplication.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: opérateurs Operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114466"
---
# <a name="operator--operators"></a>\*opérateurs opérateur

Opérateurs de multiplication

### <a name="overload-list"></a>Liste de surcharge



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Opérateur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR :: Operator * (float, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multipliez une valeur à virgule flottante par une instance de <code>XMVECTOR</code> , en retournant le résultat à une nouvelle instance de <code>XMVECTOR</code> .<br/> Le <code>operator *</code> multiplie une valeur à virgule flottante par rapport à chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a>, en retournant une nouvelle <code>XMVECTOR</code> instance dont les composants contiennent le résultat. <br/>
<blockquote>
[!Note]<br />
Cet opérateur est uniquement disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR :: Operator * (XMVECTOR, float)</strong></a></td>
<td style="text-align: left;">Multipliez une instance de <code>XMVECTOR</code> par une valeur à virgule flottante, en retournant le résultat à une nouvelle instance de <code>XMVECTOR</code> .<br/> Le <code>operator *</code> multiplie chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par une valeur à virgule flottante, en retournant une nouvelle <code>XMVECTOR</code> instance dont les composants contiennent le résultat. <br/>
<blockquote>
[!Note]<br />
Cet opérateur est uniquement disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR :: Operator * (XMVECTOR, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplie une instance de <code>XMVECTOR</code> par une deuxième instance, en retournant le résultat dans une troisième instance. <br/> Le <code>operator *</code> multiplie chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par le composant correspondant dans une deuxième instance de <code>XMVECTOR</code> , en retournant une nouvelle <code>XMVECTOR</code> instance contenant le résultat. <br/>
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

 

 
