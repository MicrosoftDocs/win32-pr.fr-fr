---
title: Bluetooth et WSASetService
description: Bluetooth utilise la fonction WSASetService pour inscrire ou supprimer une instance de service au sein de l’espace de noms Bluetooth (NS \_ BTH) à partir du Registre.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Bluetooth WSASetService
- Bluetooth et Bluetooth WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463210"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="0d438-106">Bluetooth et WSASetService</span><span class="sxs-lookup"><span data-stu-id="0d438-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="0d438-107">Bluetooth utilise la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) pour inscrire ou supprimer une instance de service au sein de l’espace de noms Bluetooth (NS \_ BTH) à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="0d438-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="0d438-108">Le handle retourné par cette opération ne peut être utilisé que pour supprimer le service.</span><span class="sxs-lookup"><span data-stu-id="0d438-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="0d438-109">Bluetooth offre deux moyens de publier des services à l’aide de la fonction [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="0d438-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="0d438-110">L’application peut demander au système de publier un enregistrement de service SDP Bluetooth simple, construit à partir de membres standard dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="0d438-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="0d438-111">L’application peut faire en sorte que le système publie son propre enregistrement SDP Bluetooth en passant une structure de [**\_ \_ service d’ensemble BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) dans le membre **lpBlob** de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="0d438-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="0d438-112">Il s’agit d’une approche plus complexe.</span><span class="sxs-lookup"><span data-stu-id="0d438-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="0d438-113">Les enregistrements SDP publiés par [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) ne sont pas conservés une fois que le processus qui les a publiés s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="0d438-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="0d438-114">L’utilisation de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) avec Bluetooth présente les exigences suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d438-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="0d438-115">Le paramètre *lpqsRegInfo* est l’adresse de la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) à inscrire.</span><span class="sxs-lookup"><span data-stu-id="0d438-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="0d438-116">Le paramètre *essOperation* est une énumération qui contient l’une des opérations répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0d438-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="0d438-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d438-117">Value</span></span>                  | <span data-ttu-id="0d438-118">Description</span><span class="sxs-lookup"><span data-stu-id="0d438-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d438-119">\_Registre RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="0d438-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="0d438-120">Démarre la publication du service sur les radios distantes qui interrogent à l’aide du protocole SDP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="0d438-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="0d438-121">\_désinscription RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="0d438-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="0d438-122">Non valide.</span><span class="sxs-lookup"><span data-stu-id="0d438-122">Not valid.</span></span> <span data-ttu-id="0d438-123">Retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0d438-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="0d438-124">RNRSERVICE \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="0d438-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="0d438-125">Arrête la publication du service.</span><span class="sxs-lookup"><span data-stu-id="0d438-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="0d438-126">Les handles de service détectés pendant un appel [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) sont incompatibles avec l’opération de suppression de RNRSERVICE \_ .</span><span class="sxs-lookup"><span data-stu-id="0d438-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="0d438-127">Le paramètre *dwControlFlags* est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0d438-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="0d438-128">Pour plus d’informations et pour obtenir la liste des options de Socket Bluetooth, consultez [options Bluetooth et Socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="0d438-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d438-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d438-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d438-130">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0d438-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 