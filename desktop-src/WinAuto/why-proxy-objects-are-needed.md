---
title: Raisons pour lesquelles les objets proxy sont nécessaires
description: Avec les objets accessibles, lorsqu’un client définit une fonction de raccordement dans le contexte, la DLL dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309998"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="a5868-103">Raisons pour lesquelles les objets proxy sont nécessaires</span><span class="sxs-lookup"><span data-stu-id="a5868-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="a5868-104">Avec les objets accessibles, lorsqu’un client définit une [fonction de raccordement dans le contexte](in-context-and-out-of-context-hook-functions.md), la dll dans laquelle la fonction de raccordement du client est implémentée est chargée dans l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="a5868-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="a5868-105">Dans ce cas, lorsque le client appelle [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) à partir de la fonction de raccordement, le pointeur d’interface qui est retourné pointe directement vers le code dans l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="a5868-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="a5868-106">Lorsque le client appelle une propriété d’interface à l’aide de ce pointeur, la bibliothèque COM (Component Object Model) n’est pas impliquée dans le marshaling ou le démarshaling et ne peut pas détecter si un objet est détruit.</span><span class="sxs-lookup"><span data-stu-id="a5868-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="a5868-107">Par conséquent, le serveur doit détecter cette situation et retourner un code d’erreur au client.</span><span class="sxs-lookup"><span data-stu-id="a5868-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




