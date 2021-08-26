---
description: Un événement de gestion de l’alimentation du système est une modification de l’état de l’alimentation du système, du mode de fonctionnement d’un appareil ou du système, ou de la valeur d’un paramètre d’alimentation.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Événements de gestion de l’alimentation du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0558dfe0c846c6b48125a382d14f03181d7f18fb2d11deb4783af975e57c4cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032929"
---
# <a name="system-power-management-events"></a>Événements de gestion de l’alimentation du système

Un événement de gestion de l’alimentation du système est une modification de l’état de l’alimentation du système, du mode de fonctionnement d’un appareil ou du système, ou de la valeur d’un paramètre d’alimentation. Étant donné que ces événements peuvent affecter le fonctionnement des applications et des pilotes installables, le système avertit toutes les applications et tous les pilotes installables en diffusant une notification pour chaque événement. Les applications et les services s’inscrivent pour les notifications à l’aide de la fonction [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Les notifications sont reçues via le message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , qui contient l’événement de gestion de l’alimentation et toutes les données associées spécifiques à l’événement.

## <a name="system-power-status-events"></a>Événements d’état de l’alimentation du système

Un *événement d’État* de l’alimentation du système se produit en cas de modification de l’alimentation ou de l’état de la batterie du système. Par exemple, le système diffuse un événement [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) chaque fois que l’utilisateur passe d’une batterie à une alimentation secteur, ou vice versa. Le système diffuse également cet événement lorsque la puissance de la batterie devient inférieure au seuil spécifié par l'utilisateur ou change selon un pourcentage spécifié.

## <a name="operational-mode-events"></a>Événements de mode opérationnel

Un *événement de mode opérationnel* se produit en cas de modification de la consommation d’énergie, comme le passage du système à un état de veille en raison d’une inactivité ou lorsque l’utilisateur met le système en veille manuellement. Le système diffuse des événements sur ces modifications avant la modification de la consommation d’énergie. Par exemple, si le système détermine qu’il est inactif, il diffuse un événement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) qui notifie les applications et les pilotes qu’il est sur le paragraphe d’interrompre l’opération et de se mettre en veille pour économiser de l’énergie. Les applications et les pilotes peuvent se préparer à la mise en veille en fermant les fichiers et en enregistrant les données pour éviter toute perte de données potentielle.

Lorsque le système effectue une *suspension critique*, le système est immédiatement mis en veille en raison d’une condition critique, telle qu’une alerte de batterie critique. Contrairement à une transition de mise en veille normale, le système ne notifie pas les applications et les pilotes avant d’effectuer une suspension critique. Par conséquent, les applications doivent être prêtes à gérer les suspensions critiques.

Lorsque l’opération système est restaurée après avoir été suspendue, le système avertit toutes les applications et tous les pilotes. Il indique également si le système reprend à partir d’une suspension critique, de sorte que l’application ou le pilote peut prendre les mesures appropriées pour restaurer ses données et poursuivre l’opération.

Les applications doivent faire chaque tentative pour gérer la transition vers l’état de veille sans intervention de l’utilisateur, car il est possible que l’utilisateur ne puisse pas répondre. Par exemple, le couvercle sur l’ordinateur Notebook peut être fermé. Lorsqu’une application reçoit une notification indiquant que le système est sur le la même de passer en mode veille, elle doit effectuer les opérations nécessaires rapidement et retourner la boucle de message. Le système autorise un maximum de deux secondes par application lors du traitement de ce message avant expiration du délai d’attente.

## <a name="power-setting-change-events"></a>Événements de modification du paramètre d’alimentation

Un événement de modification du paramètre d’alimentation se produit lorsqu’une modification est apportée à la valeur d’un paramètre d’alimentation. Par exemple, l’utilisateur modifie le mode de gestion de l’alimentation de haute performance à équilibrer dans l’application options d’alimentation du panneau de configuration. Dans ce cas, le système diffuse un événement qui indique que le mode de gestion de l’alimentation a changé. Cet événement comprend la nouvelle valeur du paramètre d’alimentation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> </dl>

 

 



