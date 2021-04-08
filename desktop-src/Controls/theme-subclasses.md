---
title: Utilisation des sous-classes Theme
description: Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672898"
---
# <a name="using-theme-subclasses"></a>Utilisation des sous-classes Theme

Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier. Par exemple, la classe **Button** est sous-classée comme afin `Start::Button` de permettre le contrôle du thème appliqué au bouton **Démarrer** .

> [!Note]  
> Soyez prudent lorsque vous créez des sous-classes comme celles présentées dans cette rubrique. Étant donné que les sous-classes peuvent être modifiées ou non disponibles dans les versions ultérieures de Windows, nous vous déconseillons de les utiliser.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Deux façons d’utiliser une sous-classe Theme

Une application peut utiliser un thème sous-classé de l’une des deux manières suivantes :

-   Elle peut utiliser la fonction [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) avec une chaîne sous la forme du `subclass::class` paramètre *pszClassList* .
-   Il peut appeler [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) avec le nom de la sous-classe theme dans le paramètre *pszSubAppName* .

## <a name="using-theme-messages-that-set-visual-style"></a>Utilisation de messages de thème qui définissent le style visuel

Certains contrôles, tels que Rebar et Toolbar, fournissent des messages spécifiques que vous pouvez envoyer pour indiquer au contrôle d’utiliser une sous-classe de thème. Pour ces contrôles, fournissez un pointeur vers une mémoire tampon qui contient le nom de la sous-classe du thème dans le paramètre *lParam* du message. Utilisez le message générique [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) ou utilisez un variant spécifique comme celui indiqué dans le tableau suivant.



| Contrôler    | Message                                             |
|------------|-----------------------------------------------------|
| Info-bulle    | [**ATTÉNUATION \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   |
| Barre d’outils    | [**TO \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

Le tableau suivant répertorie quelques-unes des sous-classes que Windows Vista définit.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Classe</th>
<th>Sous-classes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Liste déroulante</td>
<td><ul>
<li>Adresse</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>Modifier</td>
<td><ul>
<li>Adresse</li>
<li>AddressComposited</li>
<li>InactiveAddress</li>
<li>InactiveAddressComposited</li>
<li>InactiveSearchBoxEdit</li>
<li>InactiveSearchBoxEditComposited</li>
<li>MaxAddress</li>
<li>MaxAddressComposited</li>
<li>MaxInactiveAddress</li>
<li>MaxInactiveAddressComposited</li>
<li>MaxInactiveSearchBoxEdit</li>
<li>MaxInactiveSearchBoxEditComposited</li>
<li>MaxSearchBoxEdit</li>
<li>MaxSearchBoxEditComposited</li>
<li>SearchBoxEdit</li>
<li>SearchBoxEditComposited</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rebar</td>
<td><ul>
<li>BrowserTabBar</li>
<li>InactiveNavbar</li>
<li>InactiveNavbarComposited</li>
<li>MaxInactiveNavbar</li>
<li>MaxInactiveNavbarComposited</li>
<li>MaxNavbar</li>
<li>MaxNavbarComposited</li>
<li>Barre de navigation</li>
<li>NavbarComposited</li>
<li>NavbarNonTopmost</li>
</ul></td>
</tr>
<tr class="even">
<td>Onglet</td>
<td><ul>
<li>BrowserTab</li>
</ul></td>
</tr>
<tr class="odd">
<td>Barre d’outils</td>
<td><ul>
<li>Go</li>
<li>GoComposited</li>
<li>InactiveGo</li>
<li>InactiveGoComposited</li>
<li>MaxGo</li>
<li>MaxGoComposited</li>
<li>MaxInactiveGo</li>
<li>MaxInactiveGoComposited</li>
<li>Valeur SearchButton</li>
<li>SearchButtonComposited</li>
<li>Voyage</li>
<li>TravelComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a>Sous-classes Internet Explorer

Dans Windows Vista, les sous-classes de certaines classes internes à Windows Internet Explorer et l’Explorateur Windows sont disponibles, même si les classes elles-mêmes ne le sont pas. Le tableau suivant répertorie les sous-classes disponibles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AddressBand</td>
<td><ul>
<li>AB</li>
<li>ABGreen</li>
<li>ABGreenComposited</li>
<li>ABRed</li>
<li>ABRedComposited</li>
<li>ABYellow</li>
<li>ABYellowComposited</li>
</ul></td>
</tr>
<tr class="even">
<td>SearchBox</td>
<td><ul>
<li>InactiveSearchBox</li>
<li>InactiveSearchBoxComposited</li>
<li>MaxInactiveSearchBox</li>
<li>MaxInactiveSearchBoxComposited</li>
<li>MaxSearchBox</li>
<li>MaxSearchBoxComposited</li>
<li>SearchBoxComposited</li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tableau suivant présente les spécificités de ces classes.



| Contrôler     | Partie         | États                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4) |
| SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4) |



 

 

 




