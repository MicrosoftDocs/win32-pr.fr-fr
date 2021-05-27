---
title: Initialisation d’objets persistants
description: Initialisation d’objets persistants
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549195"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="4ed3e-103">Initialisation d’objets persistants</span><span class="sxs-lookup"><span data-stu-id="4ed3e-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="4ed3e-104">Plusieurs interfaces d’objets persistants, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))et [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), permettent aux clients d’initialiser des objets à un état « actualisé » ou « par défaut ».</span><span class="sxs-lookup"><span data-stu-id="4ed3e-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="4ed3e-105">Cet état initial est différent de celui d’un objet nouvellement créé, qui n’a pas d’État.</span><span class="sxs-lookup"><span data-stu-id="4ed3e-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="4ed3e-106">L’initialisation de l’état d’un objet, même à l’État par défaut, peut être une opération gourmande en ressources ou nécessitant beaucoup de ressources.</span><span class="sxs-lookup"><span data-stu-id="4ed3e-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="4ed3e-107">En séparant la création de l’initialisation, l’initialisation ne peut être effectuée que lorsqu’elle est réellement nécessaire et que les clients peuvent éviter d’initialiser les objets à l’État par défaut pour charger immédiatement les données précédemment stockées.</span><span class="sxs-lookup"><span data-stu-id="4ed3e-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed3e-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ed3e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed3e-109">Interfaces d’objets persistants</span><span class="sxs-lookup"><span data-stu-id="4ed3e-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 