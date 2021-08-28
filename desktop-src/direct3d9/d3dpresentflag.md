---
description: Constantes utilisées par les \_ paramètres D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf3a8ad3a22f5104e4d4a78d3a01a29d07d757
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624555"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Constantes utilisées par [**les \_ paramètres D3DPRESENT**](d3dpresent-parameters.md).



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Valeur</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Découpez un blit <a href="/windows/desktop/api"><strong>présent</strong></a> dans la zone cliente de la fenêtre, dans la zone de l’écran moniteur de la carte vidéo qui a créé l’appareil Direct3D. D3DPRESENTFLAG_DEVICECLIP n’est pas valide avec D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Définissez cet indicateur lors de la création de l’appareil ou de la chaîne de permutation pour activer l’abandon de la mémoire tampon z. Si cet indicateur est défini, le contenu de la mémoire tampon du stencil de profondeur n’est pas valide <a href="/windows/desktop/api"><strong>après l’appel de, ou</strong></a> <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> avec une surface de profondeur différente. L’abandon des données de la mémoire tampon z peut améliorer les performances et dépend du pilote. Le runtime de débogage applique l’élimination en effaçant la mémoire tampon z pour une valeur constante après l’appel de la <a href="/windows/desktop/api"><strong>présente</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> avec une surface de profondeur différente.<br/> La suppression des données de la mémoire tampon z est illégale pour tous les formats verrouillables, D3DFMT_D16_LOCKABLE et D3DFMT_D32F_LOCKABLE. Toute utilisation de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> qui spécifie un format verrouillable et l’abandon de la mémoire tampon z échoue. Pour plus d’informations sur les formats, consultez <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Définissez cet indicateur si l’application a besoin de pouvoir verrouiller directement la mémoire tampon d’arrière-plan. Notez que les mémoires tampons d’arrière-plan ne sont pas verrouillables, sauf si l’application spécifie D3DPRESENTFLAG_LOCKABLE_BACKBUFFER lors de l’appel de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> ou <a href="/windows/desktop/api"><strong>Reset</strong></a>. Les mémoires tampons d’arrière-plan verrouillables entraînent des coûts de performances sur certaines configurations matérielles graphiques. L’exécution d’une opération de verrouillage (ou l’utilisation de <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> pour écrire) sur la mémoire tampon d’arrière-plan verrouillable diminue les performances sur de nombreuses cartes. Dans ce cas, envisagez d’utiliser des triangles texturés pour déplacer des données vers la mémoire tampon d’arrière-plan.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Dans Direct3D9Ex, cet indicateur ne peut pas être défini si le D3DSWAPEFFECT est D3DSWAPEFFECT_FLIPEX, car le modèle de retournement permet au Gestionnaire de fenêtrage d’accéder à la mémoire tampon d’arrière-plan d’une application. Une surface partagée inter-processus ne doit pas être verrouillée.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Les analyses pivotées sont gérées automatiquement avec une copie en rotation au cours de la présentation, ce qui n’est pas très efficace. Cet indicateur signifie que l’application effectuera sa propre rotation d’affichage. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Les applications peuvent obtenir leur propre rotation éventuellement à l’aide d’une matrice de vue pivotée. Les méthodes <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> et <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> doivent être utilisées pour rechercher le paramètre de rotation actuel. Les paramètres de largeur et de hauteur de la mémoire tampon dans <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> et <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> doivent utiliser l’orientation paysage, tandis que la structure du mode plein écran doit être identique à ce qui est retourné par <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (par exemple, la largeur et la hauteur sont échangées lors d’une rotation de 90 et de 270 degrés).</p>
<p>Lors de l’utilisation du verrou sur les cibles de rendu pivotées, les hypothèses d’angle supérieur gauche ne sont plus vraies, la cible de rendu SURFACE_DESC reste paysage (comme impliqué par les paramètres de création) et la fenêtre GDI, les coordonnées de la souris, et doivent être traduites correctement quand elles sont utilisées avec la cible de rendu Direct3D et la scène.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Utilisez cet indicateur pour spécifier un mode d’affichage brut énuméré par l’adaptateur d’affichage même si Direct3D peut avoir indiqué que le mode n’est pas valide. L’application doit implémenter cela de manière fiable si le mode souhaité n’est pas vraiment valide. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Il s’agit d’un indicateur pour le pilote que les mémoires tampons d’arrière-plan contiendront des données vidéo.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Spécifie si la superposition est une plage pleine RVB ou une plage de valeurs RVB limitée. La définition de cet indicateur indique une plage limitée RVB. Dans une plage limitée, la plage RVB est compressée, de sorte que 16:16:16 est noir et 235:235:235 est blanc.
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Spécifie si la superposition est BT. 601 ou BT. 709. La définition de cet indicateur indique BT. 709, pour la télévision haute définition (HDTV).
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Spécifie si la superposition est conventionnelle YCbCr ou YCbCr étendu (xvYCC). La définition de cet indicateur indique une extension YCbCr étendue (xvYCC).
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>la définition de cet indicateur indique que le utilise permutation contient du contenu protégé et contraint automatiquement le runtime à limiter l’accès au utilise permutation afin que seul Desktop Windows Manager (DWM) puisse utiliser le utilise permutation.
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>La définition de cet indicateur indique que le pilote doit restreindre l’accès à toutes les ressources partagées créées pour l’interaction DWM. L’appelant doit créer un canal authentifié avec le pilote. Le pilote doit ensuite autoriser l’accès aux processus qui tentent d’ouvrir ces ressources partagées.
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Ces constantes sont utilisées par [**les \_ paramètres D3DPRESENT**](d3dpresent-parameters.md).

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur            |
|--------------------------|-------------|
| En-tête                   | d3d9types. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




