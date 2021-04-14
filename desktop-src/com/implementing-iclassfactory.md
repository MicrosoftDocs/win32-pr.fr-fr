---
title: Implémentation de IClassFactory
description: Implémentation de IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382919"
---
# <a name="implementing-iclassfactory"></a><span data-ttu-id="abbcd-103">Implémentation de IClassFactory</span><span class="sxs-lookup"><span data-stu-id="abbcd-103">Implementing IClassFactory</span></span>

<span data-ttu-id="abbcd-104">Lorsqu’un client utilise un CLSID pour demander la création d’une instance d’objet, la première étape est la création d’un objet de classe, un objet intermédiaire qui contient une implémentation des méthodes de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) .</span><span class="sxs-lookup"><span data-stu-id="abbcd-104">When a client uses a CLSID to request the creation of an object instance, the first step is creation of a class object, an intermediate object that contains an implementation of the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface.</span></span> <span data-ttu-id="abbcd-105">Bien que COM fournisse plusieurs fonctions de création d’instance, la première étape de l’implémentation de ces fonctions est la création d’un objet de classe.</span><span class="sxs-lookup"><span data-stu-id="abbcd-105">While COM provides several instance creation functions, the first step in the implementation of these functions is the creation of a class object.</span></span>

<span data-ttu-id="abbcd-106">Par conséquent, tous les serveurs doivent implémenter les méthodes de l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , qui contient deux méthodes :</span><span class="sxs-lookup"><span data-stu-id="abbcd-106">As a result, all servers must implement the methods of the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface, which contains two methods:</span></span>

-   <span data-ttu-id="abbcd-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="abbcd-107">[**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance).</span></span> <span data-ttu-id="abbcd-108">Cette méthode doit créer une instance non initialisée de l’objet et retourner un pointeur vers une interface demandée sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="abbcd-108">This method must create an uninitialized instance of the object and return a pointer to a requested interface on the object.</span></span>
-   <span data-ttu-id="abbcd-109">[**LockServer,**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span><span class="sxs-lookup"><span data-stu-id="abbcd-109">[**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver).</span></span> <span data-ttu-id="abbcd-110">Cette méthode incrémente simplement le nombre de références sur l’objet de classe pour s’assurer que le serveur reste en mémoire et ne s’arrête pas avant que le client ne soit prêt à le faire.</span><span class="sxs-lookup"><span data-stu-id="abbcd-110">This method just increments the reference count on the class object to ensure that the server stays in memory and does not shut down before the client is ready for it to do so.</span></span>

<span data-ttu-id="abbcd-111">Pour permettre à un serveur d’être responsable de sa propre licence, COM définit [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), qui hérite sa définition d' [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="abbcd-111">To enable a server to be responsible for its own licensing, COM defines [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), which inherits its definition from [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="abbcd-112">Ainsi, un serveur qui implémente **IClassFactory2** doit, par définition, implémenter les méthodes d' **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="abbcd-112">Thus, a server implementing **IClassFactory2** must, by definition, implement the methods of **IClassFactory**.</span></span>

<span data-ttu-id="abbcd-113">COM fournit également des fonctions d’assistance pour l’implémentation de serveurs hors processus.</span><span class="sxs-lookup"><span data-stu-id="abbcd-113">COM also provides helper functions for implementing out-of-process servers.</span></span> <span data-ttu-id="abbcd-114">Pour plus d’informations, consultez [assistance pour l’implémentation du serveur out-of-process](out-of-process-server-implementation-helpers.md).</span><span class="sxs-lookup"><span data-stu-id="abbcd-114">For more information, see [Out-of-Process Server Implementation Helpers](out-of-process-server-implementation-helpers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="abbcd-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="abbcd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abbcd-116">Responsabilités du serveur COM</span><span class="sxs-lookup"><span data-stu-id="abbcd-116">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> <dt>

[<span data-ttu-id="abbcd-117">Licences et IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="abbcd-117">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 