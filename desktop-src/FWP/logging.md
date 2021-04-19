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
# <a name="logging-windows-filtering-platform"></a>Journalisation (plateforme de filtrage Windows)

La plateforme de filtrage Windows (WFP) fournit la journalisation des rejets de paquets et des échecs IKE/AuthIP.

Les événements journalisés sont définis dans le type énuméré [**FWPM \_ NET \_ Event \_ type**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) et sont les suivants.

-   Échecs du mode principal IKE/AuthIP.
-   Échecs du mode rapide IKE/AuthIP.
-   Échecs du mode étendu AuthIP.
-   Paquets supprimés pendant la classification.
-   Paquets abandonnés par IPsec.

Par défaut, la journalisation pour WFP est activée pour les paquets entrants monodiffusion et pour tous les paquets sortants (monodiffusion, multidiffusion et diffusion). La journalisation peut être activée pour le reste des paquets, ou désactivée pour tous les paquets, via la fonction de gestion [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) . Les paramètres d’événement persistent entre les redémarrages.

Les événements journalisés sont stockés dans un journal circulaire, c’est-à-dire que les nouveaux événements remplacent les anciens lorsque le journal atteint sa taille maximale et peuvent être analysés à l’aide des fonctions de [gestion des événements](fwp-mgmt-functions.md) fournies par WFP. Le journal des événements a une taille maximale de 128 Ko et peut contenir environ 100 à 150 événements.

Les fonctions d’énumération en général, et [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) en particulier, prennent un instantané du journal au moment de la création du handle d’énumération. Les appels suivants à l’aide du même handle d’énumération retournent le jeu d’éléments suivant suivant ceux de la dernière mémoire tampon de sortie.

Lorsqu’une application désactive la journalisation WFP (en appelant [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), toutes les applications sont affectées. Le journal des événements n’est pas nettoyé jusqu’à ce qu’une application réactive la journalisation WFP, mais le journal des événements ne peut pas être interrogé avant.

Le journal des événements WFP est vidé après un redémarrage.

 

 




