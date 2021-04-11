---
title: Nettoyer les rappels d’alerte
description: Lorsque le gestionnaire de groupe de multidiffusion est informé que les destinataires quittent un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le \_ rappel de rappel d’alerte PMGM prune \_ \_ .
ms.assetid: 34eb6941-9488-481f-93ca-821789acc140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a81dab70eaded0fd1fe21bd1b5ec1b5ca495272
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029744"
---
# <a name="prune-alert-callbacks"></a><span data-ttu-id="1ca53-103">Nettoyer les rappels d’alerte</span><span class="sxs-lookup"><span data-stu-id="1ca53-103">Prune Alert Callbacks</span></span>

<span data-ttu-id="1ca53-104">Lorsque le gestionnaire de groupe de multidiffusion est informé que les destinataires quittent un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) .</span><span class="sxs-lookup"><span data-stu-id="1ca53-104">When the multicast group manager is notified that receivers are leaving a group on an interface, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback.</span></span> <span data-ttu-id="1ca53-105">Ce rappel indique aux protocoles de routage que les clients n’appartiennent plus au groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ca53-105">This callback notifies the routing protocols that clients no longer belong to the specified group.</span></span> <span data-ttu-id="1ca53-106">Par conséquent, les protocoles de routage doivent cesser de demander des données de multidiffusion pour les groupes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="1ca53-106">Therefore, the routing protocols must stop requesting multicast data for the specified groups.</span></span>

<span data-ttu-id="1ca53-107">Le gestionnaire de groupe de multidiffusion possède un ensemble prédéfini de règles utilisées pour déterminer le moment où ce rappel est appelé.</span><span class="sxs-lookup"><span data-stu-id="1ca53-107">The multicast group manager has a predefined set of rules that are used to determine when this callback is invoked.</span></span> <span data-ttu-id="1ca53-108">Ces règles sont basées sur le type de demande d’élagage envoyé par le client et l’ordre dans lequel les demandes élaguées ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="1ca53-108">These rules are based on both the type of prune request sent by the client and the order the prune requests were received in.</span></span>

## <a name="wildcard-prune-requests"></a><span data-ttu-id="1ca53-109">Demandes de nettoyage de caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1ca53-109">Wildcard Prune Requests</span></span>

<span data-ttu-id="1ca53-110">Quand un nettoyage générique d’un groupe ( \* , g) est reçu et que l’interface finale est supprimée pour l’avant-dernier client (autrement dit, lorsque les interfaces pour un seul client sont conservées), le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) sur ce client restant.</span><span class="sxs-lookup"><span data-stu-id="1ca53-110">When a wildcard prune for a group (\*, g) is received and the final interface is being removed for the second-to-last client (that is, when interfaces for only a single client remain), the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback to that remaining client.</span></span> <span data-ttu-id="1ca53-111">Après la suppression de l’interface finale pour le dernier client (autrement dit, quand aucune autre interface n’est conservée), ce rappel est appelé pour tous les autres clients inscrits auprès du gestionnaire de groupe de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="1ca53-111">After the final interface is removed for the last client (that is, when no other interfaces remain), then this callback is invoked for all the other clients that are registered with the multicast group manager.</span></span>

## <a name="source-specific-prune-requests"></a><span data-ttu-id="1ca53-112">Demandes de nettoyage Source-Specific</span><span class="sxs-lookup"><span data-stu-id="1ca53-112">Source-Specific Prune Requests</span></span>

<span data-ttu-id="1ca53-113">Lors de la réception d’un nettoyage spécifique à la source pour un ou plusieurs groupes, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) uniquement pour le client qui possède l’interface entrante vers la source.</span><span class="sxs-lookup"><span data-stu-id="1ca53-113">When a source-specific prune for a group (s, g) is received, the multicast group manager invokes the [**PMGM\_PRUNE\_ALERT\_CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) callback only for the client that owns the incoming interface towards the source s.</span></span>

 

 




