---
title: ArrowOK VML (attribut)
description: ArrowOK VML (attribut)
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382184"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="996fa-103">ArrowOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="996fa-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="996fa-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="996fa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="996fa-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="996fa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="996fa-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="996fa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="996fa-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="996fa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="996fa-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="996fa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="996fa-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="996fa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="996fa-110">Détermine si les flèches sont affichées.</span><span class="sxs-lookup"><span data-stu-id="996fa-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="996fa-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="996fa-111">Read/write.</span></span> <span data-ttu-id="996fa-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="996fa-112">**VgTriState**.</span></span>

<span data-ttu-id="996fa-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="996fa-113">**Applies To**</span></span>

[<span data-ttu-id="996fa-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="996fa-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="996fa-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="996fa-115">**Tag Syntax**</span></span>

<span data-ttu-id="996fa-116"><v : *Element* arrowok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="996fa-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="996fa-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="996fa-117">**Script Syntax**</span></span>

<span data-ttu-id="996fa-118">*Element* . arrowok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="996fa-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="996fa-119">*expression* = *élément*. arrowok</span><span class="sxs-lookup"><span data-stu-id="996fa-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="996fa-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="996fa-120">**Remarks**</span></span>

<span data-ttu-id="996fa-121">Si la **valeur est false**, le chemin d’accès ne contient pas de pointe de flèche.</span><span class="sxs-lookup"><span data-stu-id="996fa-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="996fa-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="996fa-122">The default is **False**.</span></span> <span data-ttu-id="996fa-123">Cet attribut remplace tous les autres attributs de la flèche dans l’élément parent ou **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="996fa-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="996fa-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="996fa-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="996fa-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="996fa-125">**Example**</span></span>

<span data-ttu-id="996fa-126">Le chemin d’accès n’a pas de flèche.</span><span class="sxs-lookup"><span data-stu-id="996fa-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 