---
title: Rappels du gestionnaire de groupe de multidiffusion
description: Le gestionnaire de groupe de multidiffusion utilise les rappels suivants pour notifier les clients (en général, les protocoles de routage) des événements et des modifications d’État
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842510"
---
# <a name="multicast-group-manager-callbacks"></a>Rappels du gestionnaire de groupe de multidiffusion

Le gestionnaire de groupe de multidiffusion utilise les rappels suivants pour notifier les clients (en général, les protocoles de routage) des événements et des modifications d’État :

[**\_rappel d' \_ alerte de création de PMGM \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**\_rappel d' \_ alerte de jointure PMGM \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**\_rappel d' \_ alerte PMGM prune \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**\_rappel de \_ jointure \_ locale PMGM**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**rappel de la \_ sortie locale PMGM \_ \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**\_rappel PMGM RPF \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**PMGM \_ erroné \_ si le \_ rappel**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Le gestionnaire de groupe de multidiffusion utilise les rappels suivants pour notifier IGMP des événements et des modifications d’État :

[**PMGM \_ désactiver \_ le \_ rappel IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**PMGM \_ activer \_ le \_ rappel IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 