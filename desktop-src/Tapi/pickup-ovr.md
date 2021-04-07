---
description: L’opération de collecte permet à une application de répondre à une session qui alerte à une autre adresse. L’application identifie la cible de la collecte et retourne un identificateur de session pour l’appel prélevé.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Collecte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758337"
---
# <a name="pickup"></a><span data-ttu-id="1eb16-104">Collecte</span><span class="sxs-lookup"><span data-stu-id="1eb16-104">Pickup</span></span>

<span data-ttu-id="1eb16-105">L’opération de collecte permet à une application de répondre à une session qui alerte à une autre adresse.</span><span class="sxs-lookup"><span data-stu-id="1eb16-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="1eb16-106">L’application identifie la cible de la collecte et retourne un identificateur de session pour l’appel prélevé.</span><span class="sxs-lookup"><span data-stu-id="1eb16-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="1eb16-107">Il existe plusieurs façons d’identifier la cible de la demande de cueillette.</span><span class="sxs-lookup"><span data-stu-id="1eb16-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="1eb16-108">Tout d’abord, l’application peut spécifier l’adresse du tiers d’alertes.</span><span class="sxs-lookup"><span data-stu-id="1eb16-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="1eb16-109">Deuxièmement, si aucune adresse n’est spécifiée et que le commutateur l’autorise, l’application peut récupérer toute session d’alerte dans son groupe de collecte.</span><span class="sxs-lookup"><span data-stu-id="1eb16-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="1eb16-110">Troisièmement, certains commutateurs autorisent la collecte d’une alerte de session dans un groupe de collecte différent si l’identificateur de groupe est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1eb16-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="1eb16-111">Certains systèmes téléphoniques clés prennent en charge un *transfert par le biais* de la fonctionnalité de conservation des apparences d’appel exclusives de Bridge.</span><span class="sxs-lookup"><span data-stu-id="1eb16-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="1eb16-112">Dans ce schéma, un téléphone particulier possède un appel exclusivement lorsque l’appel est actif, mais lorsque l’appel est en attente, tout téléphone ayant l’apparence de la ligne peut reprendre l’appel.</span><span class="sxs-lookup"><span data-stu-id="1eb16-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="1eb16-113">**TAPI 2. x :** Une application peut utiliser une opération de collecte avec une adresse cible **null** à cet effet, similaire à la façon dont la fonction est utilisée pour récupérer un appel d’appel en attente sur une ligne analogique.</span><span class="sxs-lookup"><span data-stu-id="1eb16-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="1eb16-114">LINEADDRFEATURE \_ PICKUPHELD indique l’existence de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1eb16-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="1eb16-115">Si LINEADDRCAPFLAGS \_ PICKUPCALLWAIT a la **valeur true**, une session peut être récupérée pour laquelle l’utilisateur a détecté de façon audible le signal d’appel en attente, mais pour lequel le fournisseur de services ne parvient pas à effectuer la détection.</span><span class="sxs-lookup"><span data-stu-id="1eb16-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="1eb16-116">Cela donne à l’utilisateur un mécanisme pour « répondre » à un appel en attente, même si le fournisseur de services n’a pas pu détecter le signal d’appel-attente.</span><span class="sxs-lookup"><span data-stu-id="1eb16-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="1eb16-117">L’adresse de destination et l’ID de groupe doivent tous deux avoir la **valeur null** pour récupérer un appel en attente d’appel.</span><span class="sxs-lookup"><span data-stu-id="1eb16-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="1eb16-118">Lorsqu’une session a été récupérée avec succès, l’application reçoit une notification de changement d’État avec la [raison](reason-ovr.md) définie sur LINECALLREASON \_ Pickup.</span><span class="sxs-lookup"><span data-stu-id="1eb16-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="1eb16-119">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.</span><span class="sxs-lookup"><span data-stu-id="1eb16-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="1eb16-120">**TAPI 2. x :** Consultez [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="1eb16-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="1eb16-121">**TAPI 3. x :** Consultez [**ITBasicCallControl ::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="1eb16-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
