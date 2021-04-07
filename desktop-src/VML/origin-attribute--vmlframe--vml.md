---
title: Origin, attribut (VMLFrame) (VML)
description: Origin, attribut (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729989"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="7f8d7-103">Origin, attribut (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="7f8d7-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="7f8d7-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7f8d7-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7f8d7-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7f8d7-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7f8d7-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7f8d7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7f8d7-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7f8d7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7f8d7-110">Définit l’origine de la zone de découpage du frame.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="7f8d7-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-111">Read/write.</span></span> <span data-ttu-id="7f8d7-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-112">**VgVector2D**.</span></span>

<span data-ttu-id="7f8d7-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7f8d7-113">**Applies To**</span></span>

[<span data-ttu-id="7f8d7-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="7f8d7-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="7f8d7-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="7f8d7-115">**Tag Syntax**</span></span>

<span data-ttu-id="7f8d7-116"><v : *élément* Origin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7f8d7-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="7f8d7-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="7f8d7-117">**Script Syntax**</span></span>

<span data-ttu-id="7f8d7-118">*Element* . Origin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7f8d7-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="7f8d7-119">*expression* = *élément*. Origin</span><span class="sxs-lookup"><span data-stu-id="7f8d7-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="7f8d7-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7f8d7-120">**Remarks**</span></span>

<span data-ttu-id="7f8d7-121">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-121">The default value is 0,0.</span></span> <span data-ttu-id="7f8d7-122">Notez que **origin** fonctionne uniquement si [clip](msdn-online-vml-clip-attribute.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="7f8d7-123">Dans cet attribut, l’origine est définie comme l’angle supérieur gauche du frame.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="7f8d7-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="7f8d7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="7f8d7-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="7f8d7-125">**Example**</span></span>

<span data-ttu-id="7f8d7-126">L’origine de la région de découpage est 100pt, 100pt.</span><span class="sxs-lookup"><span data-stu-id="7f8d7-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 