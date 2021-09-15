---
title: pack_matrix directive pragma
description: Directive pragma qui spécifie l’alignement de la compression pour les matrices.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix le HLSL de la directive pragma
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87658a9ffcf2d8715e2caa581c7127301784980c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519232"
---
# <a name="pack_matrix-pragma-directive"></a>Directive de pragma de matrice de Pack \_

Directive pragma qui spécifie l’alignement de la compression pour les matrices.



| \#matrice pragma Pack \_ ( *alignement* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>repère</em><br/></td>
<td>Alignement à définir pour les matrices. Ce paramètre peut prendre l’une des valeurs indiquées dans le tableau suivant. <br/> 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>Par défaut. Définit l’alignement de la compression de la matrice sur la colonne principale.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Définit l’alignement de la compression de la matrice sur la ligne principale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Exemples

L’exemple suivant définit l’alignement de la compression de la matrice sur la ligne principale.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Directive pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





