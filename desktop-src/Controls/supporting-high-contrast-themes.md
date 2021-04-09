---
title: Prise en charge des thèmes de contraste élevé
description: Cette rubrique compare la prise en charge des thèmes à contraste élevé dans Windows 8 à celle des versions précédentes de Windows, et explique comment prendre en charge les thèmes à contraste élevé dans une application Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842762"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="52385-103">Prise en charge des thèmes de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="52385-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="52385-104">Cette rubrique compare la prise en charge des thèmes à contraste élevé dans Windows 8 à celle des versions précédentes de Windows, et explique comment prendre en charge les thèmes à contraste élevé dans une application Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52385-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="52385-105">Il comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="52385-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="52385-106">Vue d’ensemble de la prise en charge des thèmes contraste élevé</span><span class="sxs-lookup"><span data-stu-id="52385-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="52385-107">Prise en charge des thèmes de contraste élevé dans Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="52385-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="52385-108">Ajout d’une section de compatibilité à votre manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="52385-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="52385-109">Détection des contraste élevé dans les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="52385-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="52385-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52385-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="52385-111">Vue d’ensemble de la prise en charge des thèmes contraste élevé</span><span class="sxs-lookup"><span data-stu-id="52385-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="52385-112">Windows 7 et les versions antérieures prennent en charge deux modèles de thèmes, y compris le modèle classique Windows traditionnel et les styles visuels actuels.</span><span class="sxs-lookup"><span data-stu-id="52385-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="52385-113">Le modèle Windows classique a été conservé par le biais de Windows 7 principalement pour prendre en charge les différents thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="52385-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="52385-114">Toutefois, le modèle classique de Windows présente plusieurs inconvénients :</span><span class="sxs-lookup"><span data-stu-id="52385-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="52385-115">Aucune prise en charge des thèmes utilisant des styles visuels, tels que Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="52385-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="52385-116">Les utilisateurs de thèmes à contraste élevé doivent utiliser l’interface utilisateur Windows classique.</span><span class="sxs-lookup"><span data-stu-id="52385-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="52385-117">Aucune prise en charge des fonctionnalités de l’interface utilisateur basées sur Gestionnaire de fenêtrage (DWM) à exécuter, telles que les aperçus de miniatures et la loupe plein écran introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52385-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="52385-118">Les développeurs doivent gérer deux chemins de code distincts pour prendre en charge les deux modèles différents.</span><span class="sxs-lookup"><span data-stu-id="52385-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="52385-119">Dans Windows 8 et les versions ultérieures, les modifications suivantes apportées au modèle de thème de l’utilisation répondent aux inconvénients précédents :</span><span class="sxs-lookup"><span data-stu-id="52385-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="52385-120">Le modèle Windows classique n’est plus pris en charge, ce qui permet aux développeurs de conserver un seul chemin de code pour les applications qui ciblent uniquement Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52385-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="52385-121">Étant donné que les styles visuels et le DWM sont activés dans Windows 8, les utilisateurs à contraste élevé ont accès à des fonctionnalités telles que les aperçus de miniatures et la loupe plein écran.</span><span class="sxs-lookup"><span data-stu-id="52385-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="52385-122">Les styles visuels prennent en charge la définition des couleurs de différents éléments de l’interface utilisateur, ce qui permet aux utilisateurs à contraste élevé de personnaliser l’interface utilisateur pour répondre aux besoins et aux préférences individuels.</span><span class="sxs-lookup"><span data-stu-id="52385-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="52385-123">Windows 8 prend en charge la compatibilité pour les applications existantes conçues pour utiliser des thèmes à contraste élevé basés sur le modèle Windows classique.</span><span class="sxs-lookup"><span data-stu-id="52385-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="52385-124">Prise en charge des thèmes de contraste élevé dans Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="52385-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="52385-125">Dans Windows 8, étant donné que les styles visuels sont activés en mode de contraste élevé, la prise en charge des thèmes à contraste élevé est simple, à condition que vous respectiez les indications suivantes.</span><span class="sxs-lookup"><span data-stu-id="52385-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="52385-126">Tailles des polices et des contrôles.</span><span class="sxs-lookup"><span data-stu-id="52385-126">Font and control sizes.</span></span> <span data-ttu-id="52385-127">Pour vous assurer que votre interface utilisateur est accessible aux utilisateurs handicapés, définissez les tailles de police en fonction des paramètres de thème actuels.</span><span class="sxs-lookup"><span data-stu-id="52385-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="52385-128">Définissez la taille des contrôles sur au moins la taille par défaut.</span><span class="sxs-lookup"><span data-stu-id="52385-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="52385-129">Couleurs.</span><span class="sxs-lookup"><span data-stu-id="52385-129">Colors.</span></span> <span data-ttu-id="52385-130">Évitez d’utiliser des couleurs codées en dur.</span><span class="sxs-lookup"><span data-stu-id="52385-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="52385-131">Utilisez plutôt les couleurs système, car elles sont basées sur le thème actuel.</span><span class="sxs-lookup"><span data-stu-id="52385-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="52385-132">L’utilisation de couleurs personnalisées peut interférer avec et remplacer les couleurs dans les thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="52385-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="52385-133">Manifeste d’application.</span><span class="sxs-lookup"><span data-stu-id="52385-133">Application manifest.</span></span> <span data-ttu-id="52385-134">Les applications conçues pour fonctionner avec les nouveaux thèmes à contraste élevé doivent avoir une section de compatibilité des applications définie dans le manifeste qui contient les GUID de compatibilité Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52385-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="52385-135">Dans le cas contraire, Windows suppose que l’application est conçue pour une version antérieure de Windows et restitue l’interface utilisateur de l’application en simulant le modèle Windows classique.</span><span class="sxs-lookup"><span data-stu-id="52385-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="52385-136">Ajout d’une section de compatibilité à votre manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="52385-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="52385-137">Un manifeste d’application est un fichier XML qui décrit la configuration requise pour une application.</span><span class="sxs-lookup"><span data-stu-id="52385-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="52385-138">La section compatibilité du manifeste identifie les versions de Windows prises en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="52385-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="52385-139">Les GUID suivants sont utilisés dans la section compatibilité pour identifier les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="52385-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="52385-140">Version</span><span class="sxs-lookup"><span data-stu-id="52385-140">Version</span></span>       | <span data-ttu-id="52385-141">GUID</span><span class="sxs-lookup"><span data-stu-id="52385-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="52385-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52385-142">Windows Vista</span></span> | <span data-ttu-id="52385-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="52385-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="52385-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52385-144">Windows 7</span></span>     | <span data-ttu-id="52385-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="52385-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="52385-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52385-146">Windows 8</span></span>     | <span data-ttu-id="52385-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="52385-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="52385-148">La section compatibilité peut spécifier plusieurs versions de Windows, mais chacune d’elles doit être contenue dans sa propre `<supportedOS/>` balise.</span><span class="sxs-lookup"><span data-stu-id="52385-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="52385-149">L’exemple suivant montre un manifeste d’application qui spécifie Windows 7 et Windows 8 dans la section compatibilité :</span><span class="sxs-lookup"><span data-stu-id="52385-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


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



<span data-ttu-id="52385-150">Si une application n’a pas de manifeste de compatibilité, elle est considérée comme une application Windows Vista et n’utilise pas de contrôles à thème dans la zone cliente quand un thème à contraste élevé est actif.</span><span class="sxs-lookup"><span data-stu-id="52385-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="52385-151">En outre, le comportement de certaines fonctions de style visuel est affecté.</span><span class="sxs-lookup"><span data-stu-id="52385-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="52385-152">Par exemple, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)et [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) retournent false, tandis que [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) et [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) retournent un handle null.</span><span class="sxs-lookup"><span data-stu-id="52385-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="52385-153">C’est pour la prise en charge de la compatibilité, afin que les applications générées avant Windows 8 puissent toujours restituer leur interface utilisateur de la même façon que le mode de contraste élevé des versions précédentes de Windows où les styles visuels ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="52385-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="52385-154">Sur Windows 8, l’application bénéficie toujours des avantages de la composition du poste de travail.</span><span class="sxs-lookup"><span data-stu-id="52385-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="52385-155">Cela signifie, par exemple, que les applications d’utilisation telles que la loupe plein écran ne dépendent pas de l’état du manifeste d’une application individuelle.</span><span class="sxs-lookup"><span data-stu-id="52385-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="52385-156">L’application conviviale continue de fonctionner en mode de contraste élevé avec une application qui ne s’identifie pas comme étant compatible avec Windows 8 dans son manifeste.</span><span class="sxs-lookup"><span data-stu-id="52385-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="52385-157">Les images suivantes montrent une simple boîte de dialogue avec un contraste élevé sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52385-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![HIG (boîte de dialogue)](images/win7-high-contrast.png)

<span data-ttu-id="52385-159">Cette image affiche la même boîte de dialogue avec un contraste élevé sur Windows 8, mais avec la compatibilité Windows 7 spécifiée dans le manifeste de l’application :</span><span class="sxs-lookup"><span data-stu-id="52385-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![W8, boîte de dialogue à contraste élevé](images/win7-compat.png)

<span data-ttu-id="52385-161">Cette image affiche la même boîte de dialogue avec un contraste élevé sur Windows 8, avec Windows 8 spécifié dans le manifeste de l’application :</span><span class="sxs-lookup"><span data-stu-id="52385-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![boîte de dialogue W8 à contraste élevé avec manifeste](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="52385-163">Détection des contraste élevé dans les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="52385-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="52385-164">Les applications qui s’exécutent sur des versions antérieures de Windows n’ont pas accès aux nouveaux thèmes à contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="52385-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="52385-165">Si votre application doit s’exécuter sur des versions antérieures de, vous devez inclure la prise en charge du rendu de votre interface utilisateur dans un contraWindowsst élevé dans le modèle de thèmes Windows classique.</span><span class="sxs-lookup"><span data-stu-id="52385-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="52385-166">Votre application peut déterminer si un thème à contraste élevé est actif en appelant la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) avec l’indicateur **SPI \_ GETHIGHCONTRAST** .</span><span class="sxs-lookup"><span data-stu-id="52385-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52385-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52385-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52385-168">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="52385-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="52385-169">Styles visuels</span><span class="sxs-lookup"><span data-stu-id="52385-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 