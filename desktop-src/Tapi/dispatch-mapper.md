---
description: Le mappeur de répartition est créé à l’aide de COM CoCreateInstance et expose une interface, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Mappeur de répartition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527464"
---
# <a name="dispatch-mapper"></a><span data-ttu-id="1d80b-103">Mappeur de répartition</span><span class="sxs-lookup"><span data-stu-id="1d80b-103">Dispatch Mapper</span></span>

<span data-ttu-id="1d80b-104">Le mappeur de répartition est créé à l’aide de COM **CoCreateInstance** et expose une interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span><span class="sxs-lookup"><span data-stu-id="1d80b-104">The Dispatch Mapper is created using COM **CoCreateInstance** and exposes one interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span></span> <span data-ttu-id="1d80b-105">Cette interface permet à une application de récupérer le pointeur de dispatch d’une autre interface sur un objet, en fonction du pointeur de dispatch d’une interface et du GUID d’un autre.</span><span class="sxs-lookup"><span data-stu-id="1d80b-105">This interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.</span></span> <span data-ttu-id="1d80b-106">Cette interface est fournie pour aider les programmeurs à utiliser des applications de script qui ne fournissent pas de moyen d’interroger facilement les interfaces sur un objet.</span><span class="sxs-lookup"><span data-stu-id="1d80b-106">This interface is provided to assist programmers using scripting applications which do not provide a means of readily polling the interfaces on an object.</span></span>

<span data-ttu-id="1d80b-107">Le mappeur de dispatch utilise l’interface **IObjectSafety** d’un objet pour s’assurer que l’objet est sécurisé pour l’écriture de scripts sur l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="1d80b-107">The Dispatch Mapper uses an object's **IObjectSafety** interface to make sure the object is safe for scripting on the requested interface.</span></span> <span data-ttu-id="1d80b-108">Si l’objet n’implémente pas **IObjectSafety**, ou si l’objet n’est pas sécurisé sur cette interface particulière, l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="1d80b-108">If the object does not implement **IObjectSafety**, or if the object is not safe on this particular interface, the call will fail.</span></span>

 

 



