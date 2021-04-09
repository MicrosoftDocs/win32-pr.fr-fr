---
title: Attribut maître VML
description: Attribut maître VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102316"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="fc945-103">Attribut maître VML</span><span class="sxs-lookup"><span data-stu-id="fc945-103">VML Master Attribute</span></span>

<span data-ttu-id="fc945-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fc945-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fc945-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fc945-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fc945-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="fc945-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fc945-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="fc945-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fc945-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fc945-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fc945-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fc945-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fc945-110">Détermine si un élément **Typedeforme** est un élément principal.</span><span class="sxs-lookup"><span data-stu-id="fc945-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="fc945-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fc945-111">Read/write.</span></span> <span data-ttu-id="fc945-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="fc945-112">**VgTriState**.</span></span>

<span data-ttu-id="fc945-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fc945-113">**Applies To**</span></span>

[<span data-ttu-id="fc945-114">Typedeforme</span><span class="sxs-lookup"><span data-stu-id="fc945-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="fc945-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="fc945-115">**Tag Syntax**</span></span>

<span data-ttu-id="fc945-116"><v : *Element* o :Master = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fc945-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="fc945-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="fc945-117">**Remarks**</span></span>

<span data-ttu-id="fc945-118">Si la **valeur est true**, la forme **Typedeforme** est restituée par le moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="fc945-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="fc945-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="fc945-119">The default value is **False**.</span></span>

<span data-ttu-id="fc945-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="fc945-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="fc945-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="fc945-121">**Example**</span></span>

<span data-ttu-id="fc945-122">L’élément **Typedeforme** est une forme maîtresse.</span><span class="sxs-lookup"><span data-stu-id="fc945-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 