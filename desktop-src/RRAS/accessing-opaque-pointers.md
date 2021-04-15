---
title: Accès aux pointeurs opaques
description: Les clients sont en mesure d’accéder aux informations stockées dans les destinations à l’aide de pointeurs opaques.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507307"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="b9c46-103">Accès aux pointeurs opaques</span><span class="sxs-lookup"><span data-stu-id="b9c46-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="b9c46-104">Les clients sont en mesure d’accéder aux informations stockées dans les destinations à l’aide de pointeurs opaques.</span><span class="sxs-lookup"><span data-stu-id="b9c46-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="b9c46-105">Pour utiliser le stockage, le client doit d’abord appeler [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) pour obtenir le pointeur.</span><span class="sxs-lookup"><span data-stu-id="b9c46-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="b9c46-106">Chaque fois qu’une modification apportée aux informations est nécessaire, le client doit d’abord verrouiller la destination en appelant [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) avec le paramètre *LockDest* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b9c46-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="b9c46-107">Une fois que la destination est verrouillée, le client peut apporter les modifications nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b9c46-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="b9c46-108">La destination peut être déverrouillée à l’aide d’un autre appel à **RtmLockDestination** avec le paramètre *LockDest* défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="b9c46-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="b9c46-109">La fonction [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) permet également à un client d’utiliser un verrou de lecture ou un verrou d’écriture, à l’aide du paramètre *exclusive* .</span><span class="sxs-lookup"><span data-stu-id="b9c46-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="b9c46-110">Un client doit utiliser le verrou d’écriture uniquement lorsqu’il apporte des modifications aux informations conservées à l’aide du pointeur opaque.</span><span class="sxs-lookup"><span data-stu-id="b9c46-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="b9c46-111">Les clients peuvent utiliser le verrou en lecture pour afficher les informations de pointeur opaques stockées dans une destination.</span><span class="sxs-lookup"><span data-stu-id="b9c46-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="b9c46-112">Pour obtenir un exemple de code qui montre comment utiliser ces fonctions, consultez [accéder au pointeur opaque dans une destination](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="b9c46-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




