---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953052"
---
# <a name="ajax"></a><span data-ttu-id="7bd9d-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="7bd9d-103">AJAX</span></span>

<span data-ttu-id="7bd9d-104">Les fonctionnalités AJAX dans Windows Internet Explorer 8 comme [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) et la [messagerie entre documents (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) ont des propriétés natives qui peuvent entrer en conflit avec les propriétés personnalisées existantes.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="7bd9d-105">Windows Internet Explorer expose de nouvelles propriétés pour certaines fonctionnalités AJAX, telles que la [messagerie entre documents (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), même en mode de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="7bd9d-106">Si vous ajoutez des propriétés personnalisées à l’objet d’événement, elles peuvent être en conflit avec ces nouvelles propriétés, telles que la **source**.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="7bd9d-107">L’exemple de code suivant fonctionne dans les versions antérieures d’Internet Explorer, mais pas dans les versions plus récentes, car les nouvelles fonctionnalités utilisent la propriété **source** .</span><span class="sxs-lookup"><span data-stu-id="7bd9d-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="7bd9d-108">L’exemple de code suivant montre comment vous pouvez modifier cet objet pour qu’il reste compatible.</span><span class="sxs-lookup"><span data-stu-id="7bd9d-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="7bd9d-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7bd9d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bd9d-110">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="7bd9d-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



