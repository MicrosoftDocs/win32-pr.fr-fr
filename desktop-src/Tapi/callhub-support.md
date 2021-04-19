---
description: Le suivi CallHub est une nouvelle fonctionnalité de TAPI version 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Support CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530609"
---
# <a name="callhub-support"></a><span data-ttu-id="f1580-103">Support CallHub</span><span class="sxs-lookup"><span data-stu-id="f1580-103">CallHub Support</span></span>

<span data-ttu-id="f1580-104">Le suivi CallHub est une nouvelle fonctionnalité de TAPI version 3,0.</span><span class="sxs-lookup"><span data-stu-id="f1580-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="f1580-105">La fonctionnalité CallHub a été ajoutée aux éléments de programmation TAPI 2,1 avec la remise de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f1580-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="f1580-106">Un *CallHub* représente une vue tierce d’un appel, et les handles d’appel de l’interface TAPI représentent la vue du premier tiers d’un appel.</span><span class="sxs-lookup"><span data-stu-id="f1580-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="f1580-107">Avec le suivi CallHub, le fournisseur de services est invité à suivre CallHubs et à fournir des informations sur l’appel pendant la durée de vie d’un CallHub.</span><span class="sxs-lookup"><span data-stu-id="f1580-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="f1580-108">À mesure que les nouveaux tiers joignent et laissent le CallHub, le fournisseur de services doit informer l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="f1580-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="f1580-109">Un fournisseur de services n’a pas besoin d’implémenter de nouvelles fonctions pour prendre en charge CallHub.</span><span class="sxs-lookup"><span data-stu-id="f1580-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="f1580-110">Elle doit simplement remplir le membre **dwCallID** de la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1580-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="f1580-111">Dans TAPI 3, l’interface TAPI collecte tous les appels avec le même **dwCallID** et crée un handle CallHub que l’application peut utiliser pour suivre l’appel.</span><span class="sxs-lookup"><span data-stu-id="f1580-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
