---
title: Attribut cible VML
description: Attribut cible VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512103"
---
# <a name="vml-target-attribute"></a><span data-ttu-id="49751-103">Attribut cible VML</span><span class="sxs-lookup"><span data-stu-id="49751-103">VML Target Attribute</span></span>

<span data-ttu-id="49751-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="49751-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49751-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="49751-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49751-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="49751-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49751-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="49751-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49751-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49751-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49751-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49751-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49751-110">Définit un frame ou une fenêtre dans laquelle une URL est affichée.</span><span class="sxs-lookup"><span data-stu-id="49751-110">Defines a frame or window that a URL is displayed in.</span></span> <span data-ttu-id="49751-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="49751-111">Read/write.</span></span> <span data-ttu-id="49751-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="49751-112">**String**.</span></span>

<span data-ttu-id="49751-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="49751-113">**Applies To**</span></span>

[<span data-ttu-id="49751-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="49751-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="49751-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="49751-115">**Tag Syntax**</span></span>

<span data-ttu-id="49751-116"><v : *élément* target = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="49751-116"><v: *element* target=" *expression* "></span></span>

<span data-ttu-id="49751-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="49751-117">**Remarks**</span></span>

<span data-ttu-id="49751-118">L’attribut **cible** est semblable à l’attribut **cible** HTML standard des ancres.</span><span class="sxs-lookup"><span data-stu-id="49751-118">The **Target** attribute is similar to the standard HTML **Target** attribute of anchors.</span></span>

<span data-ttu-id="49751-119">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="49751-119">Values include:</span></span>



| <span data-ttu-id="49751-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="49751-120">Value</span></span>      | <span data-ttu-id="49751-121">Description</span><span class="sxs-lookup"><span data-stu-id="49751-121">Description</span></span>                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49751-122">TargetName</span><span class="sxs-lookup"><span data-stu-id="49751-122">TargetName</span></span> | <span data-ttu-id="49751-123">Chaîne contenant le nom du frame ou de la fenêtre dans lequel charger le document.</span><span class="sxs-lookup"><span data-stu-id="49751-123">String containing the name of the frame or window in which to load the document.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="49751-124">\_Occult</span><span class="sxs-lookup"><span data-stu-id="49751-124">\_blank</span></span>    | <span data-ttu-id="49751-125">Spécifie que le document lié est chargé dans une nouvelle fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="49751-125">Specifies that the linked document is loaded into a new blank window.</span></span> <span data-ttu-id="49751-126">Cette fenêtre n’est pas nommée.</span><span class="sxs-lookup"><span data-stu-id="49751-126">This window is not named.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="49751-127">\_Media</span><span class="sxs-lookup"><span data-stu-id="49751-127">\_media</span></span>    | <span data-ttu-id="49751-128">À compter d’Internet Explorer 6 pour Windows XP Service Pack 2, l' \_ attribut Media est obsolète et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="49751-128">As of Internet Explorer 6 for Windows XP Service Pack 2, the \_media attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="49751-129">Tout d’abord disponible dans Internet Explorer 6, cette valeur spécifie que le document lié doit être chargé dans la barre de médias.</span><span class="sxs-lookup"><span data-stu-id="49751-129">First available in Internet Explorer 6, this value specified that the linked document should be loaded into the Media Bar.</span></span>                |
| <span data-ttu-id="49751-130">\_parent</span><span class="sxs-lookup"><span data-stu-id="49751-130">\_parent</span></span>   | <span data-ttu-id="49751-131">Spécifie que le document lié est chargé dans le parent immédiat du document contenant le lien.</span><span class="sxs-lookup"><span data-stu-id="49751-131">Specifies that the linked document is loaded into the immediate parent of the document containing the link.</span></span>                                                                                                                                                      |
| <span data-ttu-id="49751-132">\_recherche</span><span class="sxs-lookup"><span data-stu-id="49751-132">\_search</span></span>   | <span data-ttu-id="49751-133">À compter d’Internet Explorer 7 pour Windows XP Service Pack 2, : l' \_ attribut de recherche est obsolète et n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="49751-133">As of Internet Explorer 7 for Windows XP Service Pack 2, : The \_search attribute is obsolete and is no longer supported.</span></span> <span data-ttu-id="49751-134">Tout d’abord disponible dans Internet Explorer 6, cette valeur spécifiait que le document lié devait être chargé dans le volet de recherche du navigateur.</span><span class="sxs-lookup"><span data-stu-id="49751-134">First available in Internet Explorer 6, this value specified that the linked document was to be loaded into the browser's search pane.</span></span> |
| <span data-ttu-id="49751-135">\_self</span><span class="sxs-lookup"><span data-stu-id="49751-135">\_self</span></span>     | <span data-ttu-id="49751-136">Spécifie que le document lié est chargé dans la fenêtre dans laquelle l’utilisateur a cliqué sur le lien (fenêtre active).</span><span class="sxs-lookup"><span data-stu-id="49751-136">Specifies that the linked document is loaded into the window in which the link was clicked (the active window).</span></span>                                                                                                                                                  |
| <span data-ttu-id="49751-137">\_Retour au début</span><span class="sxs-lookup"><span data-stu-id="49751-137">\_top</span></span>      | <span data-ttu-id="49751-138">Spécifie que le document lié est chargé dans la fenêtre de premier plan.</span><span class="sxs-lookup"><span data-stu-id="49751-138">Specifies that the linked document is loaded into the topmost window.</span></span>                                                                                                                                                                                            |



 

<span data-ttu-id="49751-139">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="49751-139">*VML Standard Attribute*</span></span>

<span data-ttu-id="49751-140">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="49751-140">**Example**</span></span>

<span data-ttu-id="49751-141">Lorsque vous cliquez sur le rectangle, le navigateur charge la page d’accueil de Microsoft Corporation dans la même fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49751-141">When the rectangle is clicked, the browser loads the Microsoft Corporation home page in the same window.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="49751-142">[Exemple d’attribut cible](/previous-versions/bb264096(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49751-142">[Target Attribute Example](/previous-versions/bb264096(v=vs.85)).</span></span> <span data-ttu-id="49751-143">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="49751-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 