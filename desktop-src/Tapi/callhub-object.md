---
description: L’objet CallHub représente une vue tierce d’un appel en une partie.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objet CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952354"
---
# <a name="callhub-object"></a><span data-ttu-id="35cb6-103">Objet CallHub</span><span class="sxs-lookup"><span data-stu-id="35cb6-103">CallHub Object</span></span>

<span data-ttu-id="35cb6-104">L’objet CallHub représente une vue tierce d’un appel en une partie.</span><span class="sxs-lookup"><span data-stu-id="35cb6-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="35cb6-105">Les interfaces et les méthodes associées obtiennent et définissent des informations relatives au concentrateur, par exemple s’il est actif ou non.</span><span class="sxs-lookup"><span data-stu-id="35cb6-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="35cb6-106">À l’aide de l’objet CallHub, un utilisateur ayant la sécurité requise peut découvrir et contrôler potentiellement les autres participants dans un appel.</span><span class="sxs-lookup"><span data-stu-id="35cb6-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="35cb6-107">Un objet CallHub ne peut pas être créé directement par une application.</span><span class="sxs-lookup"><span data-stu-id="35cb6-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="35cb6-108">Un objet CallHub est créé indirectement lors de la réception d’un appel entrant via TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="35cb6-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="35cb6-109">TAPI 3 s’appuie sur les fournisseurs de services TAPI pour fournir les informations nécessaires sur les appels à implémenter à l’aide de l’objet CallHub.</span><span class="sxs-lookup"><span data-stu-id="35cb6-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="35cb6-110">Étant donné que tous les fournisseurs de services ne fournissent pas ces informations, et que tous les matériels ne prennent pas en charge le suivi des concentrateurs d’appels, les informations disponibles sur les autres utilisateurs de la connexion peuvent être limitées ou inexistantes.</span><span class="sxs-lookup"><span data-stu-id="35cb6-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="35cb6-111">L’exemple de code de [création d’une conférence simple](create-a-simple-conference.md) illustre l’utilisation d’un objet CallHub.</span><span class="sxs-lookup"><span data-stu-id="35cb6-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="35cb6-112">Consultez la page interfaces de l' [objet CallHub](callhub-object-interfaces.md) pour obtenir la liste de toutes les interfaces associées à l’objet CallHub.</span><span class="sxs-lookup"><span data-stu-id="35cb6-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



