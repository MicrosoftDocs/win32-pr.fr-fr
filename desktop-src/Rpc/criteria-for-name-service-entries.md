---
title: Critères pour les entrées de service de nom
description: Critères pour les entrées de service de nom avec appel de procédure distante (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462314"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="5700e-103">Critères pour les entrées de service de nom</span><span class="sxs-lookup"><span data-stu-id="5700e-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="5700e-104">Les critères suivants sont utilisés lors du traitement des entrées de service de nom :</span><span class="sxs-lookup"><span data-stu-id="5700e-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="5700e-105">Si vous fournissez un nom d’entrée non **null** pour [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), cette entrée sera la seule entrée recherchée pour les handles de liaison.</span><span class="sxs-lookup"><span data-stu-id="5700e-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="5700e-106">Si vous transmettez la **valeur null**, toutes les entrées de votre domaine d’ouverture de session sont recherchées.</span><span class="sxs-lookup"><span data-stu-id="5700e-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="5700e-107">Notez que cela n’inclut pas les domaines approuvés.</span><span class="sxs-lookup"><span data-stu-id="5700e-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="5700e-108">Si vous fournissez un handle d’interface, les handles de liaison sont retournés à partir d’une entrée uniquement si la section d’interface de l’entrée contient une version compatible de cet UUID d’interface.</span><span class="sxs-lookup"><span data-stu-id="5700e-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="5700e-109">Autrement dit, le numéro de version principale doit être identique à celui de l’interface UUID, tandis que le numéro de version mineure doit être supérieur ou égal au vôtre.</span><span class="sxs-lookup"><span data-stu-id="5700e-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="5700e-110">Si vous fournissez un UUID d’objet, les handles de liaison sont retournés à partir d’une entrée uniquement si la section UUID de l’objet de l’entrée contient cet UUID d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="5700e-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="5700e-111">Si une entrée de service de noms survit aux critères décrits ci-dessus, tous les descripteurs de liaison de ces entrées sont collectés.</span><span class="sxs-lookup"><span data-stu-id="5700e-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="5700e-112">Les handles avec une séquence de protocole qui n’est pas prise en charge par le client sont ignorés et les descripteurs restants sont retournés en tant que sortie de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span><span class="sxs-lookup"><span data-stu-id="5700e-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




