---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088757"
---
# <a name="ajax"></a>AJAX

Les fonctionnalités AJAX dans Windows Internet Explorer 8 comme [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) et la [messagerie entre documents (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) ont des propriétés natives qui peuvent entrer en conflit avec les propriétés personnalisées existantes.

Windows Internet Explorer expose de nouvelles propriétés pour certaines fonctionnalités AJAX, telles que la [messagerie entre documents (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), même en mode de compatibilité. Si vous ajoutez des propriétés personnalisées à l’objet d’événement, elles peuvent être en conflit avec ces nouvelles propriétés, telles que la **source**.

L’exemple de code suivant fonctionne dans les versions antérieures d’Internet Explorer, mais pas dans les versions plus récentes, car les nouvelles fonctionnalités utilisent la propriété **source** .


```JScript
event.source = myObject;
```



L’exemple de code suivant montre comment vous pouvez modifier cet objet pour qu’il reste compatible.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



