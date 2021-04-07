---
title: Énumérations de DWRITE_RENDERING_MODE
description: À compter de Windows 8, l' \_ énumération du mode de rendu DWRITE a \_ ajouté de nouvelles valeurs d’énumération et déconseillé d’autres.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2019
ms.locfileid: "103939532"
---
# <a name="dwrite_rendering_mode-enumerations"></a>\_Énumérations du mode de rendu DWRITE \_

À compter de Windows 8, l’énumération du **\_ \_ mode de rendu DWRITE** a ajouté de nouvelles valeurs d’énumération et déconseillé d’autres.

À compter de Windows 8, l’énumération du [**\_ mode DWRITE Text \_ antialias \_**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) détermine si le texte est rendu à l’aide de ClearType. Par conséquent, tous les modes de rendu ClearType dans l’énumération du **\_ \_ mode de rendu DWRITE** sont déconseillés. Ces valeurs d’énumération sont maintenant mappées à de nouveaux modes de rendu.

Le tableau ci-dessous montre les anciennes valeurs d’énumération et les nouvelles valeurs auxquelles elles sont mappées. Pour obtenir une description des nouvelles valeurs, [**consultez \_ \_ mode de rendu DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).



| Ancien mode                                                                                | Nouveau mode                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ GDI \_ classique**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**\_mode de rendu DWRITE \_ \_ GDI \_ classique**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ GDI \_ naturel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**\_mode de rendu DWRITE \_ \_ GDI \_ naturel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ naturel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ naturel**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ Natural \_ symétrique**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [**\_mode de rendu DWRITE \_ \_ CLEARTYPE \_ Natural \_ symétrique**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 et versions ultérieures)</strong></a><br/></td>
<td>Représente une méthode de rendu des glyphes. <br/>
<blockquote>
[!Note]<br />
Cette rubrique concerne <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> dans Windows 8 et versions ultérieures. Pour plus d’informations sur la version précédente, consultez <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>cette rubrique</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a><br/></td>
<td>Représente une méthode de rendu des glyphes. <br/>
<blockquote>
[!Note]<br />
Cette rubrique concerne <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> antérieure à Windows 8 et versions ultérieures. Pour plus d’informations sur la version plus récente, consultez <strong>cette rubrique</strong>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





