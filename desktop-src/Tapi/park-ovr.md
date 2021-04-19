---
description: L’opération de parc permet à une application d’envoyer une session à une adresse spéciale à laquelle elle sera conservée jusqu’à ce qu’elle soit désimmobilisée.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Parcs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518710"
---
# <a name="park"></a><span data-ttu-id="031a3-103">Parcs</span><span class="sxs-lookup"><span data-stu-id="031a3-103">Park</span></span>

<span data-ttu-id="031a3-104">L’opération de parc permet à une application d’envoyer une session à une adresse spéciale à laquelle elle sera conservée jusqu’à ce qu’elle soit désimmobilisée.</span><span class="sxs-lookup"><span data-stu-id="031a3-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="031a3-105">Du point de vue de l’application, cela ressemble à un transfert.</span><span class="sxs-lookup"><span data-stu-id="031a3-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="031a3-106">Pour le tiers situé à l’autre extrémité de la connexion, cela ressemble à la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="031a3-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="031a3-107">La différence entre le stationnement et le transfert réside dans le fait que l’adresse en stationnement n’est pas un point de connexion pour la session et que la session n’est pas avertie ou expire. La différence entre le stationnement et le blocage est qu’une fois l’opération de parc terminée, la session n’est plus associée à l’adresse de l’application.</span><span class="sxs-lookup"><span data-stu-id="031a3-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="031a3-108">Deux formes de parking une session sont fournies : le stationnement *dirigé* et le parking *indirect*.</span><span class="sxs-lookup"><span data-stu-id="031a3-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="031a3-109">Dans le parc d’appels dirigés, l’application spécifie l’adresse de destination dans laquelle l’appel doit être parqué.</span><span class="sxs-lookup"><span data-stu-id="031a3-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="031a3-110">Avec un parking indirect, le fournisseur de services ou le matériel sous-jacent détermine l’adresse et la renvoie à l’application.</span><span class="sxs-lookup"><span data-stu-id="031a3-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="031a3-111">Une session parqué passe généralement en état d’inactivité une fois qu’elle a été correctement importée, et l’application doit ensuite libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="031a3-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="031a3-112">Pour obtenir un résumé de la procédure à suivre, consultez [terminer une session](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="031a3-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="031a3-113">Si l’application désintègre la session, de nouvelles ressources de session sont allouées même si l’application a renvoyé les pointeurs précédents, si bien que l’échec des mises en production correctes peut entraîner de nombreux problèmes.</span><span class="sxs-lookup"><span data-stu-id="031a3-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="031a3-114">Certains fournisseurs de services peuvent rappeler à l’utilisateur une fois qu’une session a été immobilisée pendant un certain laps de temps.</span><span class="sxs-lookup"><span data-stu-id="031a3-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="031a3-115">L’application voit un appel d’offre avec une [raison](reason-ovr.md) d’appel définie sur rappel.</span><span class="sxs-lookup"><span data-stu-id="031a3-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="031a3-116">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="031a3-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="031a3-117">**TAPI 2. x :** Consultez [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="031a3-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="031a3-118">**TAPI 3 :** Consultez [**ITBasicCallControl ::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl ::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl :: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="031a3-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
