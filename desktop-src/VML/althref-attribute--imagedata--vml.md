---
title: Attribut AltHRef (ImageData) (VML)
description: Attribut AltHRef (ImageData) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031426"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="a1bb5-103">Attribut AltHRef (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="a1bb5-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="a1bb5-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a1bb5-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a1bb5-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a1bb5-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a1bb5-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a1bb5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a1bb5-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a1bb5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a1bb5-110">Spécifie une autre référence pour une image.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="a1bb5-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-111">Read/write.</span></span> <span data-ttu-id="a1bb5-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-112">**String**.</span></span>

<span data-ttu-id="a1bb5-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a1bb5-113">**Applies To**</span></span>

[<span data-ttu-id="a1bb5-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="a1bb5-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="a1bb5-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a1bb5-115">**Tag Syntax**</span></span>

<span data-ttu-id="a1bb5-116"><v : *Element* o :althref = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a1bb5-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="a1bb5-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="a1bb5-117">**Script Syntax**</span></span>

<span data-ttu-id="a1bb5-118">*Element* . althref = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a1bb5-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="a1bb5-119">*expression* = *élément*. althref</span><span class="sxs-lookup"><span data-stu-id="a1bb5-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="a1bb5-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a1bb5-120">**Remarks**</span></span>

<span data-ttu-id="a1bb5-121">Prend en charge la préservation des données PICT via des roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="a1bb5-122">Lors de l’écriture HTML, l’autre représentation (c’est-à-dire, les données PICT d’origine si le fichier provient du Macintosh) est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="a1bb5-123">Sur une lecture HTML, **AltHRef** est privilégié sur **src**.</span><span class="sxs-lookup"><span data-stu-id="a1bb5-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="a1bb5-124">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a1bb5-124">*Microsoft Office Extensions Attribute*</span></span>

 

 