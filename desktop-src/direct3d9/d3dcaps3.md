---
description: Indicateurs de capacité du pilote.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343364"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Indicateurs de capacité du pilote.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Valeur</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Indique que l’appareil peut respecter l’état de rendu D3DRS_ALPHABLENDENABLE en mode plein écran lors de l’utilisation de l’effet d’échange de retournement ou de suppression. Cela s’applique uniquement lorsque les États D3DRS_SRCBLEND ou D3DRS_DESTBLEND sont définis sur l’un des éléments suivants :
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>L’appareil peut accélérer la copie mémoire de la mémoire système à la mémoire vidéo locale. Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> et <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> seront accélérés par le matériel. Si cette limite est absente, ces appels échouent, mais ils sont plus lents.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>L’appareil peut accélérer la copie en mémoire de la mémoire vidéo locale jusqu’à la mémoire système. Cette limite garantit que les appels <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> seront accélérés par le matériel. Si cette limite est absente, cet appel échouera, mais sera plus lent.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>Le pilote d’affichage prend en charge l’interface DDI DXVA-HD. Pour plus d’informations sur la DDI DXVA-HD, consultez <a href="https://msdn.microsoft.com/library/dd835176.aspx">traitement d' High-Definition vidéo</a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>Indique que l’appareil peut effectuer une correction gamma à partir d’une mémoire tampon d’arrière-plan (contenant du contenu linéaire) sur un bureau sRVB.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Réservé non utilisé.</td>
</tr>
</tbody>
</table>



 

Ces constantes sont utilisées par le membre D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




