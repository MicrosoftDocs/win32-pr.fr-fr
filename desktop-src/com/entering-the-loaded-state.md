---
title: Passage à l’État chargé
description: Passage à l’État chargé
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672494"
---
# <a name="entering-the-loaded-state"></a><span data-ttu-id="ef916-103">Passage à l’État chargé</span><span class="sxs-lookup"><span data-stu-id="ef916-103">Entering the Loaded State</span></span>

<span data-ttu-id="ef916-104">Lorsqu’un objet passe à l’État chargé, les structures en mémoire représentant l’objet sont créées afin que les opérations puissent être appelées dessus.</span><span class="sxs-lookup"><span data-stu-id="ef916-104">When an object enters the loaded state, the in-memory structures representing the object are created so that operations can be invoked on it.</span></span> <span data-ttu-id="ef916-105">Le gestionnaire de l’objet ou le serveur in-process est chargé.</span><span class="sxs-lookup"><span data-stu-id="ef916-105">The object's handler or in-process server is loaded.</span></span> <span data-ttu-id="ef916-106">Ce processus, appelé *instanciation*, se produit lorsqu’un objet est chargé à partir d’un stockage persistant (transition de l’état passif à l’État chargé) ou lorsqu’un objet est créé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ef916-106">This process, referred to as *instantiation*, occurs when an object is loaded from persistent storage (a transition from the passive to the loaded state) or when an object is being created for the first time.</span></span>

<span data-ttu-id="ef916-107">En interne, l’instanciation est un processus en deux phases.</span><span class="sxs-lookup"><span data-stu-id="ef916-107">Internally, instantiation is a two-phase process.</span></span> <span data-ttu-id="ef916-108">Un objet de la classe appropriée est créé, après quoi une méthode sur cet objet est appelée pour effectuer l’initialisation et autoriser l’accès aux données de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef916-108">An object of the appropriate class is created, after which a method on that object is called to perform initialization and give access to the object's data.</span></span> <span data-ttu-id="ef916-109">La méthode d’initialisation est définie dans l’une des interfaces prises en charge par l’objet.</span><span class="sxs-lookup"><span data-stu-id="ef916-109">The initialization method is defined in one of the object's supported interfaces.</span></span> <span data-ttu-id="ef916-110">La méthode d’initialisation particulière appelée dépend du contexte dans lequel l’objet est instancié et de l’emplacement des données d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="ef916-110">The particular initialization method called depends on the context in which the object is being instantiated and the location of the initialization data.</span></span>

 

 




