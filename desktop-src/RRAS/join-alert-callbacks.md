---
title: Rappels d’alerte de jointure
description: Lorsque le gestionnaire de groupe de multidiffusion est informé qu’il existe de nouveaux récepteurs pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel d’alerte de jointure PMGM \_ \_ .
ms.assetid: b625f8ec-f59b-4151-aa38-48cf8f004966
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00dc70160b99c3cfc0e41078a3bd5882d930f31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029426"
---
# <a name="join-alert-callbacks"></a><span data-ttu-id="65a54-103">Rappels d’alerte de jointure</span><span class="sxs-lookup"><span data-stu-id="65a54-103">Join Alert Callbacks</span></span>

<span data-ttu-id="65a54-104">Lorsque le gestionnaire de groupe de multidiffusion est informé qu’il existe de nouveaux récepteurs pour un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ de jointure PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="65a54-104">When the multicast group manager is notified that there are new receivers present for a group on an interface, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback.</span></span> <span data-ttu-id="65a54-105">Ce rappel indique aux protocoles de routage que les nouveaux hôtes ont rejoint les groupes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="65a54-105">This callback notifies the routing protocols that new hosts have joined the specified groups .</span></span> <span data-ttu-id="65a54-106">Par conséquent, les protocoles de routage doivent demander des données de multidiffusion pour les groupes spécifiés par le rappel.</span><span class="sxs-lookup"><span data-stu-id="65a54-106">Therefore, the routing protocols must request multicast data for the groups specified by the callback.</span></span>

<span data-ttu-id="65a54-107">Le gestionnaire de groupe de multidiffusion utilise un ensemble prédéfini de règles utilisées pour déterminer le moment où ce rappel est appelé.</span><span class="sxs-lookup"><span data-stu-id="65a54-107">The multicast group manager uses a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="65a54-108">Cet ensemble de règles est basé sur le type de demande de jointure envoyé par le client et l’ordre dans lequel les demandes de jointure ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="65a54-108">This set of rules is based on both the type of join request sent by the client and the order the join requests were received in.</span></span>

## <a name="wildcard-join-requests"></a><span data-ttu-id="65a54-109">Demandes de jointure de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="65a54-109">Wildcard Join Requests</span></span>

<span data-ttu-id="65a54-110">Lorsqu’une jointure de caractères génériques pour un groupe ( \* , g) est reçue à partir du premier client, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM Join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) à tous les autres clients inscrits.</span><span class="sxs-lookup"><span data-stu-id="65a54-110">When a wildcard join for a group (\*, g) is received from the first client, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback to all other registered clients.</span></span> <span data-ttu-id="65a54-111">Lorsqu’une jointure de caractères génériques est reçue pour un groupe à partir du deuxième client, le gestionnaire de groupe de multidiffusion appelle ce rappel au premier client pour rejoindre le groupe.</span><span class="sxs-lookup"><span data-stu-id="65a54-111">When a wildcard join for a group is received from the second client, the multicast group manager invokes this callback to the first client to join the group.</span></span>

## <a name="source-specific-join-requests"></a><span data-ttu-id="65a54-112">Demandes de jointure Source-Specific</span><span class="sxs-lookup"><span data-stu-id="65a54-112">Source-Specific Join Requests</span></span>

<span data-ttu-id="65a54-113">Le gestionnaire de groupe de multidiffusion n’appelle pas ce rappel pour les jointures suivantes dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="65a54-113">The multicast group manager does not invoke this callback for any subsequent joins to the group.</span></span>

<span data-ttu-id="65a54-114">Lorsqu’une jointure spécifique à la source pour un ou plusieurs groupes est reçue, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM Join**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) uniquement pour le client qui possède l’interface entrante vers la source.</span><span class="sxs-lookup"><span data-stu-id="65a54-114">When a source-specific join for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_JOIN\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




