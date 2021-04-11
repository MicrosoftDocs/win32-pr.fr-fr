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
# <a name="prune-alert-callbacks"></a>Nettoyer les rappels d’alerte

Lorsque le gestionnaire de groupe de multidiffusion est informé que les destinataires quittent un groupe sur une interface, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) . Ce rappel indique aux protocoles de routage que les clients n’appartiennent plus au groupe spécifié. Par conséquent, les protocoles de routage doivent cesser de demander des données de multidiffusion pour les groupes spécifiés.

Le gestionnaire de groupe de multidiffusion possède un ensemble prédéfini de règles utilisées pour déterminer le moment où ce rappel est appelé. Ces règles sont basées sur le type de demande d’élagage envoyé par le client et l’ordre dans lequel les demandes élaguées ont été reçues.

## <a name="wildcard-prune-requests"></a>Demandes de nettoyage de caractères génériques

Quand un nettoyage générique d’un groupe ( \* , g) est reçu et que l’interface finale est supprimée pour l’avant-dernier client (autrement dit, lorsque les interfaces pour un seul client sont conservées), le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) sur ce client restant. Après la suppression de l’interface finale pour le dernier client (autrement dit, quand aucune autre interface n’est conservée), ce rappel est appelé pour tous les autres clients inscrits auprès du gestionnaire de groupe de multidiffusion.

## <a name="source-specific-prune-requests"></a>Demandes de nettoyage Source-Specific

Lors de la réception d’un nettoyage spécifique à la source pour un ou plusieurs groupes, le gestionnaire de groupe de multidiffusion appelle le rappel de [**\_ rappel d' \_ alerte \_ PMGM prune**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback) uniquement pour le client qui possède l’interface entrante vers la source.

 

 




