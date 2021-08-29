---
title: Utilisation des sous-classes Theme
description: Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9d2ad43ebd26c0e28258773b4746c597cfdc93
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480165"
---
# <a name="using-theme-subclasses"></a>Utilisation des sous-classes Theme

Les classes de thème qui représentent des contrôles tels que ComboBox, Edit, ExplorerBar, rebar, TAB et Toolbar peuvent être sous-classées afin de fournir des variations de thème pour ce contrôle particulier. Par exemple, la classe **Button** est sous-classée comme afin `Start::Button` de permettre le contrôle du thème appliqué au bouton **Démarrer** .

> [!Note]  
> Soyez prudent lorsque vous créez des sous-classes comme celles présentées dans cette rubrique. étant donné que les sous-classes peuvent être modifiées ou non disponibles dans les versions ultérieures de Windows, il est déconseillé de les utiliser.

 

## <a name="two-ways-to-use-a-theme-subclass"></a>Deux façons d’utiliser une sous-classe Theme

Une application peut utiliser un thème sous-classé de l’une des deux manières suivantes :

-   Elle peut utiliser la fonction [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) avec une chaîne sous la forme du `subclass::class` paramètre *pszClassList* .
-   Il peut appeler [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) avec le nom de la sous-classe theme dans le paramètre *pszSubAppName* .

## <a name="using-theme-messages-that-set-visual-style"></a>Utilisation de messages de thème qui définissent le style visuel

Certains contrôles, tels que Rebar et Toolbar, fournissent des messages spécifiques que vous pouvez envoyer pour indiquer au contrôle d’utiliser une sous-classe de thème. Pour ces contrôles, fournissez un pointeur vers une mémoire tampon qui contient le nom de la sous-classe du thème dans le paramètre *lParam* du message. Utilisez le message générique [**CCM \_ SETWINDOWTHEME**](ccm-setwindowtheme.md) ou utilisez un variant spécifique comme celui indiqué dans le tableau suivant.



| Control    | Message                                             |
|------------|-----------------------------------------------------|
| Info-bulle    | [**ATTÉNUATION \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   |
| Barre d’outils    | [**TO \_ SETWINDOWTHEME**](tb-setwindowtheme.md)     |
| Rebar      | [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     |
| ComboBoxEx | [**CBEM \_ SETWINDOWTHEME**](cbem-setwindowtheme.md) |



 

le tableau suivant répertorie certaines des sous-classes que Windows Vista définit.




| Classe | Sous-classes | 
|-------|------------|
| Liste déroulante | <ul><li>Adresse</li><li>AddressComposited</li><li>InactiveAddress</li><li>InactiveAddressComposited</li><li>MaxAddress</li><li>MaxAddressComposited</li><li>MaxInactiveAddress</li><li>MaxInactiveAddressComposited</li></ul> | 
| Modifier | <ul><li>Adresse</li><li>AddressComposited</li><li>InactiveAddress</li><li>InactiveAddressComposited</li><li>InactiveSearchBoxEdit</li><li>InactiveSearchBoxEditComposited</li><li>MaxAddress</li><li>MaxAddressComposited</li><li>MaxInactiveAddress</li><li>MaxInactiveAddressComposited</li><li>MaxInactiveSearchBoxEdit</li><li>MaxInactiveSearchBoxEditComposited</li><li>MaxSearchBoxEdit</li><li>MaxSearchBoxEditComposited</li><li>SearchBoxEdit</li><li>SearchBoxEditComposited</li></ul> | 
| Rebar | <ul><li>BrowserTabBar</li><li>InactiveNavbar</li><li>InactiveNavbarComposited</li><li>MaxInactiveNavbar</li><li>MaxInactiveNavbarComposited</li><li>MaxNavbar</li><li>MaxNavbarComposited</li><li>Barre de navigation</li><li>NavbarComposited</li><li>NavbarNonTopmost</li></ul> | 
| Onglet | <ul><li>BrowserTab</li></ul> | 
| Barre d’outils | <ul><li>Go</li><li>GoComposited</li><li>InactiveGo</li><li>InactiveGoComposited</li><li>MaxGo</li><li>MaxGoComposited</li><li>MaxInactiveGo</li><li>MaxInactiveGoComposited</li><li>Valeur SearchButton</li><li>SearchButtonComposited</li><li>Voyage</li><li>TravelComposited</li></ul> | 




 

## <a name="internet-explorer-subclasses"></a>Sous-classes Internet Explorer

dans Windows Vista, les sous-classes de certaines classes internes à Windows Internet explorer et l’explorateur de Windows sont disponibles, même si les classes elles-mêmes ne le sont pas. Le tableau suivant répertorie les sous-classes disponibles.




| | | AddressBand | <ul><li>AB</li><li>ABGreen</li><li>ABGreenComposited</li><li>ABRed</li><li>ABRedComposited</li><li>ABYellow</li><li>ABYellowComposited</li></ul> | | SearchBox | <ul><li>InactiveSearchBox</li><li>InactiveSearchBoxComposited</li><li>MaxInactiveSearchBox</li><li>MaxInactiveSearchBoxComposited</li><li>MaxSearchBox</li><li>MaxSearchBoxComposited</li><li>SearchBoxComposited</li></ul> | 




 

Le tableau suivant présente les spécificités de ces classes.



| Control     | Partie         | États                                                 |
|-------------|--------------|--------------------------------------------------------|
| ADDRESSBAND | ABBACKGROUND | NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4) |
| SEARCHBOX   | SBBACKGROUND | NORMAL (0x1), chaud (0X2), désactivé (0x3), ayant le focus (0x4) |



 

 

 




