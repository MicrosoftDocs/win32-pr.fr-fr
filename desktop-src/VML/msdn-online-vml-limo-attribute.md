---
title: Limo VML (attribut)
description: Limo VML (attribut)
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382019"
---
# <a name="vml-limo-attribute"></a><span data-ttu-id="e636f-103">Limo VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="e636f-103">VML Limo Attribute</span></span>

<span data-ttu-id="e636f-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e636f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e636f-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e636f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e636f-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e636f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e636f-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e636f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e636f-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e636f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e636f-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e636f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e636f-110">Définit un point d’étirement sur le tracé.</span><span class="sxs-lookup"><span data-stu-id="e636f-110">Defines a stretch point on the path.</span></span> <span data-ttu-id="e636f-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e636f-111">Read/write.</span></span> <span data-ttu-id="e636f-112">**Vector2d**.</span><span class="sxs-lookup"><span data-stu-id="e636f-112">**Vector2D**.</span></span>

<span data-ttu-id="e636f-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e636f-113">**Applies To**</span></span>

[<span data-ttu-id="e636f-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="e636f-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="e636f-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e636f-115">**Tag Syntax**</span></span>

<span data-ttu-id="e636f-116"><v : *Element* Limo = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e636f-116"><v: *element* limo=" *expression* "></span></span>

<span data-ttu-id="e636f-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="e636f-117">**Script Syntax**</span></span>

<span data-ttu-id="e636f-118">*Element* . Limo = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e636f-118">*element* .limo="*expression*"</span></span>

<span data-ttu-id="e636f-119">*expression* = *élément*. Limo</span><span class="sxs-lookup"><span data-stu-id="e636f-119">*expression*=*element*.limo</span></span>

<span data-ttu-id="e636f-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e636f-120">**Remarks**</span></span>

<span data-ttu-id="e636f-121">La valeur par défaut est « 0 0 ».</span><span class="sxs-lookup"><span data-stu-id="e636f-121">The default value is "0 0".</span></span> <span data-ttu-id="e636f-122">Les étirements Limo sont des points sur le bord d’une forme qui définissent où et comment une forme peut être étirée par un utilisateur dans un éditeur graphique.</span><span class="sxs-lookup"><span data-stu-id="e636f-122">Limo stretches are points on a shape's edge that define where and how a shape may be stretched by a user in a graphical editor.</span></span>

<span data-ttu-id="e636f-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="e636f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e636f-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e636f-124">**Example**</span></span>

<span data-ttu-id="e636f-125">Un point d’étirement de Limo est défini à mi-chemin le long de la ligne horizontale.</span><span class="sxs-lookup"><span data-stu-id="e636f-125">A limo stretch point is defined halfway along the horizontal line.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 