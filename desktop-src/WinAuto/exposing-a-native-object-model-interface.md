---
title: Exposition d’une interface de modèle objet natif
description: Si un élément d’interface utilisateur prend en charge un modèle d’objet natif autre que Microsoft Active Accessibility ou UI Automation, il peut exposer l’interface personnalisée en répondant aux \_ messages WM GETOBJECT qui incluent l' \_ identificateur d’objet objid NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029440"
---
# <a name="exposing-a-native-object-model-interface"></a><span data-ttu-id="9d4d6-103">Exposition d’une interface de modèle objet natif</span><span class="sxs-lookup"><span data-stu-id="9d4d6-103">Exposing a Native Object Model Interface</span></span>

<span data-ttu-id="9d4d6-104">Si un élément d’interface utilisateur prend en charge un modèle d’objet natif autre que Microsoft Active Accessibility ou UI Automation, il peut exposer l’interface personnalisée en répondant aux messages [**WM \_ GETOBJECT**](wm-getobject.md) qui incluent l’identificateur d’objet [**objID \_ NATIVEOM**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="9d4d6-104">If a UI element supports a native object model other than Microsoft Active Accessibility or UI Automation, it can expose the custom interface by responding to [**WM\_GETOBJECT**](wm-getobject.md) messages that include the [**OBJID\_NATIVEOM**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="9d4d6-105">Pour répondre, l’élément d’interface utilisateur doit retourner la valeur récupérée par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .</span><span class="sxs-lookup"><span data-stu-id="9d4d6-105">To respond, the UI element should return the value retrieved by a call to the [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) function.</span></span>

<span data-ttu-id="9d4d6-106">Un client peut récupérer une interface à partir d’un élément d’interface utilisateur qui prend en charge un modèle objet natif en appelant la fonction [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et en spécifiant [**objID \_ NATIVEOM**](object-identifiers.md) comme deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="9d4d6-106">A client can retrieve an interface from a UI element that supports a native object model by calling the [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) function and specifying [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

 

 




