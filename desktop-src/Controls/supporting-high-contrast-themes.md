---
title: Prise en charge des thèmes de contraste élevé
description: cette rubrique compare la prise en charge des thèmes à contraste élevé dans Windows 8 à celle des versions précédentes de Windows, et explique comment prendre en charge les thèmes à contraste élevé dans une application Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116909"
---
# <a name="supporting-high-contrast-themes"></a>Prise en charge des thèmes de contraste élevé

cette rubrique compare la prise en charge des thèmes à contraste élevé dans Windows 8 à celle des versions précédentes de Windows, et explique comment prendre en charge les thèmes à contraste élevé dans une application Windows 8.

Il comprend les sections suivantes.

-   [Vue d’ensemble de la prise en charge des thèmes contraste élevé](#overview-of-support-for-high-contrast-themes)
-   [prise en charge des thèmes de contraste élevé dans Windows 8 et versions ultérieures](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [Ajout d’une section de compatibilité à votre manifeste d’application](#adding-a-compatibility-section-to-your-application-manifest)
-   [Détection des contraste élevé dans les versions précédentes de Windows](#detecting-high-contrast-in-previous-versions-of-windows)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>Vue d’ensemble de la prise en charge des thèmes contraste élevé

Windows 7 et les versions antérieures prennent en charge deux modèles de thèmes, y compris le modèle classique Windows classique et les styles visuels actuels. le modèle Windows classique a été conservé par le biais de Windows 7 principalement pour prendre en charge les différents thèmes à contraste élevé. toutefois, le Windows modèle classique présente plusieurs inconvénients :

-   aucune prise en charge des thèmes qui utilisent des styles visuels, tels que Windows Aero. les utilisateurs de thèmes à contraste élevé doivent utiliser le Windows interface utilisateur classique.
-   aucune prise en charge des fonctionnalités de l’interface utilisateur basées sur Gestionnaire de fenêtrage (DWM) à exécuter, telles que les aperçus de miniatures et la loupe plein écran introduite dans Windows 7.
-   Les développeurs doivent gérer deux chemins de code distincts pour prendre en charge les deux modèles différents.

dans Windows 8 et versions ultérieures, les modifications suivantes apportées au modèle de thèmes réagit aux inconvénients précédents :

-   le modèle de thèmes classiques Windows n’est plus pris en charge, ce qui permet aux développeurs de conserver un seul chemin de code pour les applications qui ciblent uniquement les Windows 8.
-   étant donné que les styles visuels et DWM se trouvent dans Windows 8, les utilisateurs à contraste élevé ont accès à des fonctionnalités telles que les aperçus de miniatures et la loupe plein écran.
-   Les styles visuels prennent en charge la définition des couleurs de différents éléments de l’interface utilisateur, ce qui permet aux utilisateurs à contraste élevé de personnaliser l’interface utilisateur pour répondre aux besoins et aux préférences individuels.
-   Windows 8 prend en charge la compatibilité pour les applications existantes conçues pour utiliser des thèmes à contraste élevé basés sur le modèle d’utilisation classique Windows.

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>prise en charge des thèmes de contraste élevé dans Windows 8 et versions ultérieures

dans Windows 8, étant donné que les styles visuels sont activés en mode de contraste élevé, la prise en charge des thèmes à contraste élevé est simple, à condition que vous respectiez les instructions suivantes.

-   Tailles des polices et des contrôles. Pour vous assurer que votre interface utilisateur est accessible aux utilisateurs handicapés, définissez les tailles de police en fonction des paramètres de thème actuels. Définissez la taille des contrôles sur au moins la taille par défaut.
-   Couleurs. Évitez d’utiliser des couleurs codées en dur. Utilisez plutôt les couleurs système, car elles sont basées sur le thème actuel. L’utilisation de couleurs personnalisées peut interférer avec et remplacer les couleurs dans les thèmes à contraste élevé.
-   Manifeste d’application. les applications conçues pour fonctionner avec les nouveaux thèmes à contraste élevé doivent avoir une section de compatibilité des applications définie dans le manifeste qui contient les guid de compatibilité Windows 8. dans le cas contraire, Windows suppose que l’application est conçue pour une version antérieure de Windows et restitue l’interface utilisateur de l’application en simulant le Windows modèle de thèmes classiques.

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>Ajout d’une section de compatibilité à votre manifeste d’application

Un manifeste d’application est un fichier XML qui décrit la configuration requise pour une application. la section compatibilité du manifeste identifie les versions de Windows prises en charge par l’application. Les GUID suivants sont utilisés dans la section compatibilité pour identifier les différentes versions de Windows.

| Version       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

la section compatibilité peut spécifier plusieurs versions de Windows, mais chacune d’elles doit être contenue dans sa propre `<supportedOS/>` balise. l’exemple suivant montre un manifeste d’application qui spécifie Windows 7 et Windows 8 dans la section compatibilité :


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



si une application n’a pas de manifeste de compatibilité, elle est supposée être une application Windows Vista et n’utilise pas de contrôles à thème dans la zone cliente quand un thème à contraste élevé est actif. En outre, le comportement de certaines fonctions de style visuel est affecté. Par exemple, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)et [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) retournent false, tandis que [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) et [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) retournent un handle null. cela est destiné à la prise en charge de la compatibilité, afin que les applications générées avant Windows 8 puissent toujours restituer leur interface utilisateur de la même façon que le mode de contraste élevé des versions précédentes de Windows où les styles visuels ne sont pas disponibles.

sur Windows 8, l’application bénéficie toujours des avantages de la composition du bureau. Cela signifie, par exemple, que les applications d’utilisation telles que la loupe plein écran ne dépendent pas de l’état du manifeste d’une application individuelle. l’application conviviale continue de fonctionner en mode de contraste élevé avec une application qui ne s’identifie pas comme étant Windows 8 compatible dans son manifeste.

les images suivantes montrent une simple boîte de dialogue à contraste élevé sur Windows 7.

![HIG (boîte de dialogue)](images/win7-high-contrast.png)

cette image affiche la même boîte de dialogue dans un contraste élevé sur Windows 8, mais avec la compatibilité Windows 7 spécifiée dans le manifeste de l’application :

![W8, boîte de dialogue à contraste élevé](images/win7-compat.png)

cette image affiche la même boîte de dialogue avec un contraste élevé sur Windows 8, avec Windows 8 spécifié dans le manifeste de l’application :

![boîte de dialogue W8 à contraste élevé avec manifeste](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>Détection des contraste élevé dans les versions précédentes de Windows

les Applications qui s’exécutent sur des versions antérieures de Windows n’ont pas accès aux nouveaux thèmes à contraste élevé. si votre application doit s’exécuter sur des versions antérieures de, vous devez inclure la prise en charge du rendu de votre interface utilisateur dans le contraWindowsst élevé dans le modèle de thèmes classiques Windows. Votre application peut déterminer si un thème à contraste élevé est actif en appelant la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec l’indicateur **SPI \_ GETHIGHCONTRAST** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation des styles visuels](cookbook-overview.md)
</dt> <dt>

[Styles visuels](themes-overview.md)
</dt> </dl>

 

 