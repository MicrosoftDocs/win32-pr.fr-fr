---
title: Localisation d’un objet distant
description: Localisation d’un objet distant
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842806"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="7f916-103">Localisation d’un objet distant</span><span class="sxs-lookup"><span data-stu-id="7f916-103">Locating a Remote Object</span></span>

<span data-ttu-id="7f916-104">Avec l’avènement de COM pour les systèmes distribués, COM utilise le modèle de base pour la création d’objets décrit dans [objets de classe com et CLSID](com-class-objects-and-clsids.md) et ajoute plusieurs méthodes pour localiser un objet qui peut résider sur un autre système d’un réseau, sans surcharger l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="7f916-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="7f916-105">COM a ajouté des clés de Registre qui permettent à un serveur d’enregistrer le nom de l’ordinateur sur lequel il réside ou sur l’ordinateur où se trouve un stockage existant.</span><span class="sxs-lookup"><span data-stu-id="7f916-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="7f916-106">Par conséquent, les applications clientes doivent connaître uniquement le CLSID du serveur.</span><span class="sxs-lookup"><span data-stu-id="7f916-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="7f916-107">Toutefois, dans les cas où il est souhaité, COM a remplacé un paramètre précédemment réservé de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) par une structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , qui permet à un client de spécifier l’emplacement d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="7f916-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="7f916-108">Une autre valeur importante dans la fonction **CoGetClassObject** est l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , qui spécifie si l’objet attendu doit être exécuté in-process, local hors processus ou distant hors processus.</span><span class="sxs-lookup"><span data-stu-id="7f916-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="7f916-109">Pris ensemble, ces deux valeurs et les valeurs dans le registre déterminent comment et où l’objet doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="7f916-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="7f916-110">Les appels de création d’instance, lorsqu’ils spécifient un emplacement de serveur, peuvent remplacer un paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="7f916-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="7f916-111">L’algorithme utilisé par COM pour ce faire est décrit dans la référence de l’énumération [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .</span><span class="sxs-lookup"><span data-stu-id="7f916-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="7f916-112">L’activation à distance dépend de la relation de sécurité entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="7f916-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="7f916-113">Pour plus d’informations, consultez [sécurité dans com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="7f916-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f916-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f916-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f916-115">Objets de classe COM et CLSID</span><span class="sxs-lookup"><span data-stu-id="7f916-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="7f916-116">Création d’un objet à l’aide d’un objet de classe</span><span class="sxs-lookup"><span data-stu-id="7f916-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 