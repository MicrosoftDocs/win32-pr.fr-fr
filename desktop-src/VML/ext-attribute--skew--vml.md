---
title: Attribut ext (skew) (VML)
description: Attribut ext (skew) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199295"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="6df52-103">Attribut ext (skew) (VML)</span><span class="sxs-lookup"><span data-stu-id="6df52-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="6df52-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6df52-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6df52-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6df52-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6df52-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6df52-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6df52-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6df52-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6df52-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6df52-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6df52-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6df52-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6df52-110">Définit le mode d’affichage d’une inclinaison.</span><span class="sxs-lookup"><span data-stu-id="6df52-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="6df52-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6df52-111">Read/write.</span></span> <span data-ttu-id="6df52-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="6df52-112">**String**.</span></span>

<span data-ttu-id="6df52-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6df52-113">**Applies To**</span></span>

[<span data-ttu-id="6df52-114">Appliquez</span><span class="sxs-lookup"><span data-stu-id="6df52-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="6df52-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="6df52-115">**Tag Syntax**</span></span>

<span data-ttu-id="6df52-116"><o : *Element* v :ext = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6df52-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="6df52-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="6df52-117">**Script Syntax**</span></span>

<span data-ttu-id="6df52-118">*Element* . ext = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6df52-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="6df52-119">*expression* = *élément*. ext</span><span class="sxs-lookup"><span data-stu-id="6df52-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="6df52-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="6df52-120">**Remarks**</span></span>

<span data-ttu-id="6df52-121">Cet attribut est utilisé pour indiquer aux éditeurs graphiques comment traiter l’élément **skew** .</span><span class="sxs-lookup"><span data-stu-id="6df52-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="6df52-122">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="6df52-122">Values include:</span></span>

-   <span data-ttu-id="6df52-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="6df52-123">**edit**</span></span>
-   <span data-ttu-id="6df52-124">**affichage** (par défaut)</span><span class="sxs-lookup"><span data-stu-id="6df52-124">**view** (default)</span></span>
-   <span data-ttu-id="6df52-125">**backwardCompatible**</span><span class="sxs-lookup"><span data-stu-id="6df52-125">**backwardCompatible**</span></span>

<span data-ttu-id="6df52-126">Si une extension est définie sur **modifier**, elle peut être ignorée par une visionneuse de logiciel.</span><span class="sxs-lookup"><span data-stu-id="6df52-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="6df52-127">Si la valeur est définie sur **View**, la visionneuse doit restituer la représentation bitmap à la place.</span><span class="sxs-lookup"><span data-stu-id="6df52-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="6df52-128">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="6df52-128">*Microsoft Office Extensions Attribute*</span></span>

 

 