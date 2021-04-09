---
title: Galerie de Drop-Down
description: La Galerie de Drop-Down se compose d’un bouton qui, lorsque vous cliquez dessus, affiche une liste déroulante contenant une collection d’éléments ou de commandes s’excluant mutuellement.
ms.assetid: 10644e10-f903-49f6-aecd-1a63d97fe447
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07553dcc767b50786e271544ea44bd17670a2a9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732205"
---
# <a name="drop-down-gallery"></a>Galerie de Drop-Down

La Galerie de Drop-Down se compose d’un bouton qui, lorsque vous cliquez dessus, affiche une liste déroulante contenant une collection d’éléments ou de commandes s’excluant mutuellement.

-   [Détails](#details)
-   [Propriétés de la Galerie déroulante](#drop-down-gallery-properties)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

Ce contrôle est utile pour exposer des éléments ou des commandes connexes dans lesquels il n’existe aucune valeur par défaut évidente, et les éléments individuels peuvent être représentés par une image, du texte, ou les deux.

La prise en charge des barres de redimensionnement verticale et des angles, ou des poignées de redimensionnement, est assurée par le biais de l’élément [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) .

La capture d’écran suivante illustre la Galerie du ruban Drop-Down dans Microsoft Paint.

![capture d’écran d’un contrôle dropdowngallery dans le ruban Microsoft Paint.](images/controls/dropdowngallery.png)

## <a name="drop-down-gallery-properties"></a>Propriétés de la Galerie de Drop-Down

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle Drop-Down Gallery.

En général, une propriété de la Galerie de Drop-Down est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle Drop-Down Gallery.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Clé de propriété</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(valide uniquement pour une galerie d’éléments)<br/></td>
<td>Prend en charge <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework :: GetUICommandProperty</strong></a> et <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework :: SetUICommandProperty</strong></a>.
<blockquote>
[!Note]<br />
Si la commande associée au contrôle est invalidée via un appel à <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework :: InvalidateUICommand</strong></a>, le Framework interroge cette propriété lorsque <code>UI_INVALIDATIONS_VALUE</code> est passé comme valeur d' <em>indicateurs</em>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Peut uniquement être mis à jour par le biais d’une invalidation.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bibliothèque de contrôles de l’infrastructure du ruban Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage DropDownGallery**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[Exemple de Galerie](windowsribbon-gallerysample.md)
</dt> </dl>

