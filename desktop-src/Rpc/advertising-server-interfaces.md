---
title: Interfaces de serveur de publicité
description: Le côté serveur d’une application qui utilise des handles automatiques doit appeler la fonction RpcNsBindingExport pour rendre les informations de liaison relatives au serveur disponibles pour les clients.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029257"
---
# <a name="advertising-server-interfaces"></a><span data-ttu-id="74be9-103">Interfaces de serveur de publicité</span><span class="sxs-lookup"><span data-stu-id="74be9-103">Advertising Server Interfaces</span></span>

<span data-ttu-id="74be9-104">Le côté serveur d’une application qui utilise des handles automatiques doit appeler la fonction [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) pour rendre les informations de liaison relatives au serveur disponibles pour les clients.</span><span class="sxs-lookup"><span data-stu-id="74be9-104">The server side of an application that uses automatic handles must call the function [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) to make binding information about the server available to clients.</span></span> <span data-ttu-id="74be9-105">Les handles de liaison automatiques requièrent un service de nom s’exécutant sur un serveur accessible au client.</span><span class="sxs-lookup"><span data-stu-id="74be9-105">Automatic binding handles require a name service running on a server that is accessible to the client.</span></span> <span data-ttu-id="74be9-106">L’implémentation Microsoft du service de noms, Microsoft Locator, gère les handles automatiques.</span><span class="sxs-lookup"><span data-stu-id="74be9-106">The Microsoft implementation of the name service, Microsoft Locator, manages automatic handles.</span></span> <span data-ttu-id="74be9-107">Les applications serveur qui utilisent des handles de liaison implicites et explicites peuvent également annoncer leur présence dans la base de données de service de noms.</span><span class="sxs-lookup"><span data-stu-id="74be9-107">Server applications that use implicit and explicit binding handles can also advertise their presence in the name service database.</span></span>

<span data-ttu-id="74be9-108">En règle générale, le serveur appelle les fonctions d’exécution suivantes :</span><span class="sxs-lookup"><span data-stu-id="74be9-108">Typically, the server calls the following run-time functions:</span></span>

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

<span data-ttu-id="74be9-109">Les appels aux deux premières fonctions dans ce fragment de code sont similaires à l' [exemple Hello, World](tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="74be9-109">The calls to the first two functions in this code fragment are similar to the [Hello, World example](tutorial.md).</span></span> <span data-ttu-id="74be9-110">Ces fonctions rendent les informations relatives à la liaison disponibles pour le client.</span><span class="sxs-lookup"><span data-stu-id="74be9-110">These functions make information about the binding available to the client.</span></span> <span data-ttu-id="74be9-111">Les appels à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) et [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) placent les informations dans la base de données de service de noms.</span><span class="sxs-lookup"><span data-stu-id="74be9-111">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) put the information in the name service database.</span></span> <span data-ttu-id="74be9-112">L’appel à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) remplit le vecteur de liaison avec des handles de liaison valides avant l’exportation des handles vers le service de noms.</span><span class="sxs-lookup"><span data-stu-id="74be9-112">The call to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) fills the binding vector with valid binding handles before the handles are exported to the name service.</span></span> <span data-ttu-id="74be9-113">Une fois que le programme serveur a exporté les descripteurs vers la base de données, le client (ou stubs client) peut appeler [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) et [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) pour obtenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="74be9-113">After the server program exports the handles to the database, the client (or client stubs) can call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) and [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) to obtain this information.</span></span> <span data-ttu-id="74be9-114">Pour plus d’informations, consultez [recherche de systèmes hôtes serveur](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="74be9-114">For details, see [Finding Server Host Systems](finding-server-host-systems.md).</span></span>

<span data-ttu-id="74be9-115">Les appels à [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) et [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) et leurs structures de données associées se présentent comme suit :</span><span class="sxs-lookup"><span data-stu-id="74be9-115">The calls to [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) and [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) and their associated data structures look similar to the following:</span></span>

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

<span data-ttu-id="74be9-116">Notez que le [](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) paramètre RpcServerInqBindings *pBindingVector* est un pointeur vers un pointeur vers [**un \_ \_ vecteur de liaison RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span><span class="sxs-lookup"><span data-stu-id="74be9-116">Note that the [**RpcServerInqBindings**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) parameter *pBindingVector* is a pointer to a pointer to [**RPC\_BINDING\_VECTOR**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector).</span></span> <span data-ttu-id="74be9-117">Souvenez-vous également que chaque appel à [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) doit être suivi d’un appel à [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span><span class="sxs-lookup"><span data-stu-id="74be9-117">Also remember that each call to [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) must be followed by a call to [**RpcBindingVectorFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).</span></span>

<span data-ttu-id="74be9-118">Pour supprimer l’interface exportée de la base de données de service de noms, le serveur appelle [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="74be9-118">To remove the exported interface from the name service database, the server calls [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) as shown:</span></span>

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

<span data-ttu-id="74be9-119">La fonction [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) doit être utilisée uniquement lorsque le service est définitivement supprimé.</span><span class="sxs-lookup"><span data-stu-id="74be9-119">The [**RpcNsBindingUnexport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) function should be used only when the service is being permanently removed.</span></span> <span data-ttu-id="74be9-120">Il ne doit pas être utilisé lorsque le service est temporairement désactivé, par exemple quand le serveur est arrêté à des fins de maintenance.</span><span class="sxs-lookup"><span data-stu-id="74be9-120">It should not be used when the service is temporarily disabled, such as when the server is shut down for maintenance.</span></span> <span data-ttu-id="74be9-121">Un programme serveur peut s’inscrire auprès de la base de données de service de noms, mais n’est pas disponible car le serveur est temporairement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="74be9-121">A server program can register itself with the name service database, yet be unavailable because the server is temporarily offline.</span></span> <span data-ttu-id="74be9-122">L’application cliente doit contenir le code de gestion des exceptions pour une telle condition.</span><span class="sxs-lookup"><span data-stu-id="74be9-122">The client application should contain exception-handling code for such a condition.</span></span>

<span data-ttu-id="74be9-123">Pour plus d’informations sur le contenu et le format de la base de données de service de noms, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="74be9-123">For more information on the content and format of the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="74be9-124">Les applications peuvent utiliser le service Active Directory si les programmes client et serveur s’exécutent sous Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="74be9-124">Applications can utilize the Active Directory service if both the client and server programs are running under Windows 2000.</span></span> <span data-ttu-id="74be9-125">Les ordinateurs qui exécutent les programmes client et serveur doivent tous deux être membres d’un domaine Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="74be9-125">The computers running the client and server programs must both be members of a Windows 2000 domain.</span></span>

<span data-ttu-id="74be9-126">Pour annoncer sa présence à l’aide du service Active Directory, le programme serveur doit s’exécuter dans le contexte de sécurité d’un administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="74be9-126">To advertise its presence using the Active Directory service, the server program should run in the security context of a domain administrator.</span></span> <span data-ttu-id="74be9-127">S’il s’exécute dans le contexte des utilisateurs du domaine, un administrateur de domaine doit modifier la liste de contrôle d’accès (ACL) sur le conteneur des services RPC.</span><span class="sxs-lookup"><span data-stu-id="74be9-127">If it is running in the context of domain users, a domain administrator must modify the access control list (ACL) on the RPC Services container.</span></span> <span data-ttu-id="74be9-128">Pour plus d’informations, consultez la documentation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="74be9-128">For more information, see the Active Directory documentation.</span></span>

 

 




