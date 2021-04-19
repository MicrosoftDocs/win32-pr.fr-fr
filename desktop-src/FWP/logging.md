---
title: Journalisation (plateforme de filtrage Windows)
description: La plateforme de filtrage Windows (WFP) fournit la journalisation des rejets de paquets et des échecs IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512539"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="c64f2-103">Journalisation (plateforme de filtrage Windows)</span><span class="sxs-lookup"><span data-stu-id="c64f2-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="c64f2-104">La plateforme de filtrage Windows (WFP) fournit la journalisation des rejets de paquets et des échecs IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c64f2-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="c64f2-105">Les événements journalisés sont définis dans le type énuméré [**FWPM \_ NET \_ Event \_ type**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) et sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="c64f2-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="c64f2-106">Échecs du mode principal IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c64f2-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="c64f2-107">Échecs du mode rapide IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c64f2-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="c64f2-108">Échecs du mode étendu AuthIP.</span><span class="sxs-lookup"><span data-stu-id="c64f2-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="c64f2-109">Paquets supprimés pendant la classification.</span><span class="sxs-lookup"><span data-stu-id="c64f2-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="c64f2-110">Paquets abandonnés par IPsec.</span><span class="sxs-lookup"><span data-stu-id="c64f2-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="c64f2-111">Par défaut, la journalisation pour WFP est activée pour les paquets entrants monodiffusion et pour tous les paquets sortants (monodiffusion, multidiffusion et diffusion).</span><span class="sxs-lookup"><span data-stu-id="c64f2-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="c64f2-112">La journalisation peut être activée pour le reste des paquets, ou désactivée pour tous les paquets, via la fonction de gestion [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) .</span><span class="sxs-lookup"><span data-stu-id="c64f2-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="c64f2-113">Les paramètres d’événement persistent entre les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="c64f2-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="c64f2-114">Les événements journalisés sont stockés dans un journal circulaire, c’est-à-dire que les nouveaux événements remplacent les anciens lorsque le journal atteint sa taille maximale et peuvent être analysés à l’aide des fonctions de [gestion des événements](fwp-mgmt-functions.md) fournies par WFP.</span><span class="sxs-lookup"><span data-stu-id="c64f2-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="c64f2-115">Le journal des événements a une taille maximale de 128 Ko et peut contenir environ 100 à 150 événements.</span><span class="sxs-lookup"><span data-stu-id="c64f2-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="c64f2-116">Les fonctions d’énumération en général, et [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) en particulier, prennent un instantané du journal au moment de la création du handle d’énumération.</span><span class="sxs-lookup"><span data-stu-id="c64f2-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="c64f2-117">Les appels suivants à l’aide du même handle d’énumération retournent le jeu d’éléments suivant suivant ceux de la dernière mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="c64f2-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="c64f2-118">Lorsqu’une application désactive la journalisation WFP (en appelant [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), toutes les applications sont affectées.</span><span class="sxs-lookup"><span data-stu-id="c64f2-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="c64f2-119">Le journal des événements n’est pas nettoyé jusqu’à ce qu’une application réactive la journalisation WFP, mais le journal des événements ne peut pas être interrogé avant.</span><span class="sxs-lookup"><span data-stu-id="c64f2-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="c64f2-120">Le journal des événements WFP est vidé après un redémarrage.</span><span class="sxs-lookup"><span data-stu-id="c64f2-120">The WFP event log is emptied after a reboot.</span></span>

 

 




