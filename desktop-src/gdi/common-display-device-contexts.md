---
description: Un contexte de périphérique courant est utilisé pour le dessin dans la zone cliente de la fenêtre.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Contextes de périphérique d’affichage courants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890b0235784ec1ed11c8ce3a553244629a008d75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236484"
---
# <a name="common-display-device-contexts"></a>Contextes de périphérique d’affichage courants

Un *contexte de périphérique courant* est utilisé pour le dessin dans la zone cliente de la fenêtre. Le système fournit par défaut un contexte de périphérique commun pour toute fenêtre dont la classe de fenêtre ne spécifie pas explicitement un style de contexte de périphérique d’affichage. Les contextes de périphérique courants sont généralement utilisés avec des fenêtres qui peuvent être dessinées sans modification étendue des attributs de contexte de périphérique. Les contextes de périphérique courants sont pratiques, car ils ne nécessitent pas de ressources mémoire ou système supplémentaires, mais ils peuvent être gênants si l’application doit configurer de nombreux attributs avant de les utiliser.

Le système récupère tous les contextes de périphérique courants à partir du cache de contexte de périphérique d’affichage. Une application peut récupérer un contexte de périphérique commun immédiatement après la création de la fenêtre. Étant donné que le contexte de périphérique commun provient du cache, l’application doit toujours libérer le contexte de périphérique dès que possible après le dessin. Une fois le contexte de périphérique commun libéré, il n’est plus valide et l’application ne doit pas essayer de le dessiner. Pour redessiner, l’application doit récupérer un nouveau contexte de périphérique courant et continuer à récupérer et à libérer un contexte de périphérique courant chaque fois qu’elle est dessinée dans la fenêtre. Si l’application récupère le handle de contexte de périphérique à l’aide de la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , elle doit utiliser la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) pour libérer le handle. De même, pour chaque fonction [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , l’application doit utiliser une fonction [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) correspondante.

Lorsque l’application récupère le contexte de périphérique, le système ajuste l’origine pour qu’elle s’aligne avec l’angle supérieur gauche de la zone cliente. Il définit également la zone de découpage afin que la sortie vers le contexte de périphérique soit découpée vers la zone cliente. Toute sortie qui apparaîtrait autrement en dehors de la zone cliente est découpée. Si l’application récupère le contexte de périphérique courant à l’aide de [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), le système comprend également la région de mise à jour dans la zone de découpage pour restreindre davantage la sortie.

Quand une application libère un contexte de périphérique courant, le système restaure les valeurs par défaut pour les attributs du contexte de périphérique. Une application qui modifie des valeurs d’attribut doit le faire à chaque fois qu’elle récupère un contexte de périphérique commun. Le fait de libérer le contexte de périphérique libère tous les objets de dessin que l’application y a peut-être sélectionnés, de sorte que l’application n’a pas besoin de libérer ces objets avant de libérer le contexte de périphérique. Dans tous les cas, une application ne doit jamais supposer que le contexte de périphérique commun conserve les sélections non par défaut après sa libération.

 

 



