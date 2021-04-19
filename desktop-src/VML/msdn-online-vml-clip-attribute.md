---
title: Attribut de clip VML
description: Attribut de clip VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511498"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="c7916-103">Attribut de clip VML</span><span class="sxs-lookup"><span data-stu-id="c7916-103">VML Clip Attribute</span></span>

<span data-ttu-id="c7916-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c7916-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7916-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c7916-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7916-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c7916-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7916-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c7916-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7916-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7916-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7916-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7916-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7916-110">Détermine si le découpage est activé.</span><span class="sxs-lookup"><span data-stu-id="c7916-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="c7916-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c7916-111">Read/write.</span></span> <span data-ttu-id="c7916-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c7916-112">**VgTriState**.</span></span>

<span data-ttu-id="c7916-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c7916-113">**Applies To**</span></span>

[<span data-ttu-id="c7916-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="c7916-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="c7916-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c7916-115">**Tag Syntax**</span></span>

<span data-ttu-id="c7916-116"><v : *Element* clip = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c7916-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="c7916-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c7916-117">**Script Syntax**</span></span>

<span data-ttu-id="c7916-118">*Element* . clip = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c7916-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="c7916-119">*expression* = *élément*. clip</span><span class="sxs-lookup"><span data-stu-id="c7916-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="c7916-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c7916-120">**Remarks**</span></span>

<span data-ttu-id="c7916-121">Si **clip** a la **valeur false**, la forme est mise à l’échelle pour s’ajuster au cadre.</span><span class="sxs-lookup"><span data-stu-id="c7916-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="c7916-122">Si la **valeur est true**, toutes les parties de la forme qui sont en dehors du frame ne seront pas affichées.</span><span class="sxs-lookup"><span data-stu-id="c7916-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="c7916-123">Notez que [origin](origin-attribute--vmlframe--vml.md) et [Size](size-attribute--vmlframe.md) ne sont pas utilisés, sauf si **clip** a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="c7916-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="c7916-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c7916-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c7916-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c7916-125">**Example**</span></span>

<span data-ttu-id="c7916-126">L’image définie dans le fichier externe sera découpée.</span><span class="sxs-lookup"><span data-stu-id="c7916-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 