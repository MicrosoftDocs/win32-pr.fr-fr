---
title: Arrêt, suspension et reprise d’un appareil
description: Arrêt, suspension et reprise d’un appareil
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Commande MCI_STOP
- Commande MCI_PAUSE
- Commande MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5485365a6c846556a1037f55a0b211755ce0f93162bc6720c7241353fc8625b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037099"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Arrêt, suspension et reprise d’un appareil

La commande [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) interrompt la diffusion ou l’enregistrement d’un appareil. De nombreux appareils prennent également en charge la commande [**Pause**](pause.md) ([**\_ Pause MCI**](mci-pause.md)). La différence entre l' **arrêt** et la **Pause** dépend de l’appareil. En règle générale, **suspendre** l’opération interrompt, mais laisse l’appareil prêt à reprendre la lecture ou l’enregistrement immédiatement.

L’utilisation de la commande [**lire**](play.md) ([**\_ lecture MCI**](mci-play.md)) ou [**Enregistrer**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) pour redémarrer un appareil réinitialise les emplacements spécifiés avec les indicateurs « to » (MCI \_ à) et « from » (MCI \_ à partir de) avant la suspension ou l’arrêt de l’appareil. Sans l’indicateur « from », ces commandes réinitialisent l’emplacement de départ à la position actuelle. Sans l’indicateur « to », ils réinitialisent l’emplacement de fin à la fin du support. Pour poursuivre la lecture ou l’enregistrement sans réinitialiser une position d’arrêt précédemment spécifiée, utilisez l’indicateur « to » de la commande **Play** ou **Record** pour spécifier une position de fin.

Certains appareils prennent en charge la commande de [**reprise**](resume.md) ([**\_ Resume MCI**](mci-resume.md)) pour redémarrer un appareil suspendu. Cette commande ne change pas les emplacements « to » et « from » spécifiés avec la commande **Play** ou **Record** qui a précédé la commande [**Pause**](pause.md) .

 

 




