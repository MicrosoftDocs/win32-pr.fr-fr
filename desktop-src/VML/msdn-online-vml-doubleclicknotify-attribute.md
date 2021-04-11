---
title: DoubleClickNotify VML (attribut)
description: DoubleClickNotify VML (attribut)
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315234"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="110a5-103">DoubleClickNotify VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="110a5-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="110a5-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="110a5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="110a5-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="110a5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="110a5-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="110a5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="110a5-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="110a5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="110a5-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="110a5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="110a5-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="110a5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="110a5-110">Envoie un message d’événement lors d’un double-clic sur une forme.</span><span class="sxs-lookup"><span data-stu-id="110a5-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="110a5-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="110a5-111">Read/write.</span></span> <span data-ttu-id="110a5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="110a5-112">**VgTriState**.</span></span>

<span data-ttu-id="110a5-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="110a5-113">**Applies To**</span></span>

[<span data-ttu-id="110a5-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="110a5-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="110a5-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="110a5-115">**Tag Syntax**</span></span>

<span data-ttu-id="110a5-116"><v : *Element* o :doubleclicknotify = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="110a5-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="110a5-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="110a5-117">**Remarks**</span></span>

<span data-ttu-id="110a5-118">La valeur par défaut est **false**, ce qui indique que l’événement ne sera pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="110a5-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="110a5-119">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="110a5-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="110a5-120">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="110a5-120">**Example**</span></span>

<span data-ttu-id="110a5-121">La forme déclenche un événement de double-clic lorsque vous double-cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="110a5-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 