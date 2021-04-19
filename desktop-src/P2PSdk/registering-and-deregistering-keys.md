---
description: Inscription et annulation de l’inscription des clés
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Inscription et annulation de l’inscription des clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532137"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="6e6fd-103">Inscription et annulation de l’inscription des clés</span><span class="sxs-lookup"><span data-stu-id="6e6fd-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="6e6fd-104">Enregistrement des clés</span><span class="sxs-lookup"><span data-stu-id="6e6fd-104">Registering Keys</span></span>

<span data-ttu-id="6e6fd-105">Un nœud peut enregistrer des clés avec [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) à tout moment dans les États réseau **DRT \_ actif**, **DRT \_ seul** et **DRT \_ \_ non** .</span><span class="sxs-lookup"><span data-stu-id="6e6fd-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="6e6fd-106">Les clés inscrites en **DRT \_** uniquement et **DRT \_ aucun état \_ réseau** ne peuvent être reconnues par d’autres DRTs une fois que le nœud local est passé à **DRT \_ actif**.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="6e6fd-107">Les clés identiques ne peuvent pas être inscrites dans la même instance DRT lors de l’utilisation de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span><span class="sxs-lookup"><span data-stu-id="6e6fd-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="6e6fd-108">Si l’inscription de clés identiques est tentée, l’inscription de la deuxième clé échoue.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="6e6fd-109">L’utilisation de clés identiques doit également être évitée entre différentes instances DRT.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="6e6fd-110">Recherche par rapport à la désignation de clé unique ces clés identiques peuvent retourner l’une des clés, quelles que soient les données associées à la clé.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="6e6fd-111">Si un comportement différent est requis pour l’implémentation, un fournisseur de sécurité peut être créé à la place de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) pour prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="6e6fd-112">Annulation de l’inscription des clés</span><span class="sxs-lookup"><span data-stu-id="6e6fd-112">Deregistering Keys</span></span>

<span data-ttu-id="6e6fd-113">Un nœud peut annuler l’inscription d’une clé à chaque fois qu’elle a été inscrite.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="6e6fd-114">Toutefois, seule l’application qui a inscrit la clé peut la supprimer.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="6e6fd-115">Une application peut annuler l’inscription d’une clé à partir du nœud local à l’aide de la fonction [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) .</span><span class="sxs-lookup"><span data-stu-id="6e6fd-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="6e6fd-116">Une fois l’opération terminée, la fonction déclenche un événement de **\_ \_ \_ \_ modification de clé LEAFSET d’événement DRT** , en informant l’application et les autres nœuds qui participent à la maille DRT.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="6e6fd-117">Dans l’état **d' \_ erreur DRT** , l’appel requis de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) entraînera l’annulation de l’inscription de toutes les clés par l’infrastructure DRT.</span><span class="sxs-lookup"><span data-stu-id="6e6fd-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e6fd-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e6fd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6fd-119">Recherche dans une table de routage distribuée</span><span class="sxs-lookup"><span data-stu-id="6e6fd-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="6e6fd-120">À propos des tables de routage distribuées</span><span class="sxs-lookup"><span data-stu-id="6e6fd-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="6e6fd-121">Référence de API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="6e6fd-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



