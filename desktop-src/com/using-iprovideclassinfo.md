---
title: Utilisation de IProvideClassInfo
description: Utilisation de IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031929"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="4f3a1-103">Utilisation de IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="4f3a1-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="4f3a1-104">Un objet connectable peut offrir les interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) et [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) afin que ses clients puissent examiner facilement ses informations de type.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="4f3a1-105">Cette fonctionnalité est importante pour traiter les interfaces sortantes, qui, par définition, sont définies par un objet mais implémentées par un client sur son propre objet récepteur.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="4f3a1-106">Dans certains cas, une interface sortante est connue au moment de la compilation pour l’objet connectable et l’objet récepteur. C’est le cas avec [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="4f3a1-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="4f3a1-107">Dans d’autres cas, toutefois, seul l’objet connectable connaît ses définitions d’interface sortantes au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="4f3a1-108">Dans ce cas, le client doit obtenir les informations de type pour l’interface sortante afin qu’il puisse fournir dynamiquement un récepteur prenant en charge les points d’entrée corrects, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4f3a1-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="4f3a1-109">Le client énumère les points de connexion, puis, pour obtenir les IID des interfaces sortantes prises en charge par l’objet connectable, appelle [**IConnectionPoint :: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) pour chaque point de connexion.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="4f3a1-110">Le client interroge l’objet connectable pour l’une des interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .</span><span class="sxs-lookup"><span data-stu-id="4f3a1-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="4f3a1-111">Le client appelle les méthodes dans les interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) pour obtenir les informations de type pour l’interface sortante.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="4f3a1-112">Le client crée un objet récepteur qui prend en charge l’interface sortante.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="4f3a1-113">Le processus se poursuit et le client appelle [**IConnectionPoint :: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) pour connecter son récepteur au point de connexion.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="4f3a1-114">Dans les informations de type, la [**source**](/windows/desktop/Midl/source) d’attribut marque une [**interface**](/windows/desktop/Midl/interface) ou [**dispinterface**](/windows/desktop/Midl/dispinterface) listée sous une [**coclasse**](/windows/desktop/Midl/coclass) comme une interface sortante.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="4f3a1-115">Ceux qui sont répertoriés sans cet attribut sont considérés comme des interfaces entrantes.</span><span class="sxs-lookup"><span data-stu-id="4f3a1-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f3a1-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f3a1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f3a1-117">Interfaces d’objets connectables</span><span class="sxs-lookup"><span data-stu-id="4f3a1-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4f3a1-118">Fournir des informations sur la classe</span><span class="sxs-lookup"><span data-stu-id="4f3a1-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 