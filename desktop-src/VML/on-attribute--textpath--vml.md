---
title: Sur l’attribut (TextPath) (VML)
description: Sur l’attribut (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508117"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="612d6-103">Sur l’attribut (TextPath) (VML)</span><span class="sxs-lookup"><span data-stu-id="612d6-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="612d6-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="612d6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="612d6-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="612d6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="612d6-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="612d6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="612d6-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="612d6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="612d6-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="612d6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="612d6-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="612d6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="612d6-110">Définit si le texte est affiché.</span><span class="sxs-lookup"><span data-stu-id="612d6-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="612d6-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="612d6-111">Read/write.</span></span> <span data-ttu-id="612d6-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="612d6-112">**VgTriState**.</span></span>

<span data-ttu-id="612d6-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="612d6-113">**Applies To**</span></span>

[<span data-ttu-id="612d6-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="612d6-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="612d6-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="612d6-115">**Tag Syntax**</span></span>

<span data-ttu-id="612d6-116"><v : *Element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="612d6-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="612d6-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="612d6-117">**Script Syntax**</span></span>

<span data-ttu-id="612d6-118">*Element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="612d6-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="612d6-119">*expression* = *élément*. on</span><span class="sxs-lookup"><span data-stu-id="612d6-119">*expression*=*element*.on</span></span>

<span data-ttu-id="612d6-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="612d6-120">**Remarks**</span></span>

<span data-ttu-id="612d6-121">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="612d6-121">Default is **False**.</span></span> <span data-ttu-id="612d6-122">Cette valeur doit être définie sur **true** pour afficher du texte sur un tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="612d6-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="612d6-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="612d6-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="612d6-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="612d6-124">**Example**</span></span>

<span data-ttu-id="612d6-125">Le texte du tracé de texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="612d6-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 