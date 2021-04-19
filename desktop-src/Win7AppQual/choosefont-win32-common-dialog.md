---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () boîte de dialogue commune Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530269"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="26acc-103">ChooseFont () boîte de dialogue commune Win32</span><span class="sxs-lookup"><span data-stu-id="26acc-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="26acc-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="26acc-104">Affected Platforms</span></span>

<span data-ttu-id="26acc-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="26acc-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="26acc-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26acc-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="26acc-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="26acc-107">Feature Impact</span></span>

<span data-ttu-id="26acc-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="26acc-108">**Severity** - Low</span></span>  
<span data-ttu-id="26acc-109">**Fréquence** -moyenne</span><span class="sxs-lookup"><span data-stu-id="26acc-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="26acc-110">Description</span><span class="sxs-lookup"><span data-stu-id="26acc-110">Description</span></span>

<span data-ttu-id="26acc-111">Windows 7 comprend plusieurs mises à jour de la boîte de dialogue commune Win32 ChooseFont ().</span><span class="sxs-lookup"><span data-stu-id="26acc-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="26acc-112">Elles se répartissent en deux catégories :</span><span class="sxs-lookup"><span data-stu-id="26acc-112">These fall into two categories:</span></span>

-   <span data-ttu-id="26acc-113">Actualisation visuelle de la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="26acc-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="26acc-114">Prise en charge des nouvelles fonctionnalités afficher/masquer les polices</span><span class="sxs-lookup"><span data-stu-id="26acc-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="26acc-115">La **boîte de dialogue actualiser** met à jour le modèle standard pour que la boîte de dialogue soit plus en ligne avec d’autres dispositions de dialogue dans Windows.</span><span class="sxs-lookup"><span data-stu-id="26acc-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="26acc-116">Il introduit le WYSIWYG dans les listes d’affichage des polices pour aider les utilisateurs à choisir des polices.</span><span class="sxs-lookup"><span data-stu-id="26acc-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="26acc-117">Il comprend également un lien vers le CPL des polices pour fournir un accès facile aux utilisateurs souhaitant personnaliser leurs listes de polices.</span><span class="sxs-lookup"><span data-stu-id="26acc-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="26acc-118">**Afficher/masquer les polices** est une nouvelle fonctionnalité de la plateforme Windows 7, dans laquelle les polices non appropriées pour les paramètres de langue de l’utilisateur actuel (méthodes d’entrée) ne sont pas présentées par défaut dans les listes de sélection de polices.</span><span class="sxs-lookup"><span data-stu-id="26acc-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="26acc-119">Les utilisateurs peuvent personnaliser les polices qu’ils souhaitent voir apparaître dans le CPL des polices ou désactiver cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="26acc-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="26acc-120">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="26acc-120">Manifestation of Impact</span></span>

<span data-ttu-id="26acc-121">**Actualisation visuelle de la boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="26acc-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="26acc-122">Nous avons introduit deux nouveaux modèles dans Windows 7 (un pour les applications qui chargent la version 6 ou ultérieure de comctl32.dll et une autre pour les applications qui chargent des versions antérieures).</span><span class="sxs-lookup"><span data-stu-id="26acc-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="26acc-123">Pour des raisons de compatibilité des applications, ces nouveaux modèles sont chargés uniquement pour les applications qui ne raccordent pas la file d’attente de messages ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="26acc-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="26acc-124">Les applications qui raccordent la file d’attente de messages continuent de voir l’ancienne disposition de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="26acc-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="26acc-125">Les applications qui fournissent leurs propres modèles continuent à pouvoir les utiliser.</span><span class="sxs-lookup"><span data-stu-id="26acc-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="26acc-126">Les applications qui n’obtiennent pas les nouveaux modèles ne voient pas les modifications de disposition de la boîte de dialogue à partir de Vista.</span><span class="sxs-lookup"><span data-stu-id="26acc-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="26acc-127">Ils doivent toutefois toujours obtenir la nouvelle version préliminaire de la police WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="26acc-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="26acc-128">**Afficher/masquer les polices**</span><span class="sxs-lookup"><span data-stu-id="26acc-128">**Show/hide fonts**</span></span>

<span data-ttu-id="26acc-129">Pour toutes les versions de ChooseFont, la boîte de dialogue utilisera les paramètres afficher/masquer la police de l’utilisateur actuel pour déterminer la liste de polices à afficher.</span><span class="sxs-lookup"><span data-stu-id="26acc-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="26acc-130">Cela entraîne l’affichage de moins de listes de polices dans la plupart des instances.</span><span class="sxs-lookup"><span data-stu-id="26acc-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="26acc-131">Atténuation des utilisateurs finaux</span><span class="sxs-lookup"><span data-stu-id="26acc-131">End-user Mitigation</span></span>

<span data-ttu-id="26acc-132">**Afficher/masquer les polices :** Pour désactiver le masquage de la police, les utilisateurs doivent accéder à la page Paramètres des polices dans le CPL des polices et désélectionner l’option</span><span class="sxs-lookup"><span data-stu-id="26acc-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="26acc-133">Case à cocher « Masquer les polices en fonction des paramètres de langue »</span><span class="sxs-lookup"><span data-stu-id="26acc-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="26acc-134">Atténuation des développeurs</span><span class="sxs-lookup"><span data-stu-id="26acc-134">Developer Mitigation</span></span>

-   <span data-ttu-id="26acc-135">**Actualisation visuelle :** Les développeurs d’applications qui fournissent leurs propres modèles peuvent souhaiter l’actualiser pour qu’ils soient conformes au nouveau modèle Windows 7 approprié.</span><span class="sxs-lookup"><span data-stu-id="26acc-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="26acc-136">Les nouveaux modèles sont disponibles dans le fichier de modèle font. dlg.</span><span class="sxs-lookup"><span data-stu-id="26acc-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="26acc-137">**Remarque :** Le nouveau modèle publié contient un contrôle SysLink supplémentaire qui fournit un raccourci permettant aux utilisateurs de lancer le CPL des polices pour afficher plus de polices.</span><span class="sxs-lookup"><span data-stu-id="26acc-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="26acc-138">Le contrôle de lien requiert la version 6 de la bibliothèque de contrôles communs Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="26acc-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="26acc-139">Les développeurs doivent fournir un manifeste ou une directive qui spécifie l’utilisation de la version 6 de la DLL si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="26acc-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="26acc-140">Lorsqu’une application utilise une version antérieure de la bibliothèque de contrôles communs, utilisez le type de contrôle « PUSHBUTTON » à la place.</span><span class="sxs-lookup"><span data-stu-id="26acc-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="26acc-141">**Afficher/masquer les polices :** Les développeurs peuvent désactiver cette fonctionnalité en fournissant un indicateur supplémentaire (CF \_ INACTIVEFONTS) dans le membre Flags de la structure CHOOSEFONT.</span><span class="sxs-lookup"><span data-stu-id="26acc-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="26acc-142">La définition de cet indicateur entraîne l’affichage de toutes les polices installées dans la liste police.</span><span class="sxs-lookup"><span data-stu-id="26acc-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="26acc-143">**Afficher/masquer les polices :** Les applications qui fournissent du contenu d’aide ChooseFont peuvent souhaiter ajouter du contenu pour expliquer pourquoi la liste de polices est réduite et diriger les utilisateurs vers le CPL des polices pour personnaliser leurs listes de polices.</span><span class="sxs-lookup"><span data-stu-id="26acc-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="26acc-144">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="26acc-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="26acc-145">Les développeurs dont les applications raccordent la file d’attente de messages ChooseFont pour personnaliser la boîte de dialogue doivent vérifier que leurs applications conservent toutes les fonctionnalités existantes.</span><span class="sxs-lookup"><span data-stu-id="26acc-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="26acc-146">Les applications qui découpent fortement la liste de polices à l’aide d’indicateurs doivent s’assurer que la liste de polices présentée reste acceptable.</span><span class="sxs-lookup"><span data-stu-id="26acc-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



