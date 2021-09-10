---
title: Interrogation et définition du tempo
description: Interrogation et définition du tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (Musical Instrument Digital Interface), tempo
- MIDI (Musical Instrument Digital Interface), tempo
- Séquenceur MIDI MCI, tempo
- Commande MCI_STATUS
- tempo de séquence
- tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364544"
---
# <a name="querying-and-setting-the-tempo"></a>Interrogation et définition du tempo

Pour récupérer le tempo d’une séquence, utilisez la commande [**MCI \_ Status**](mci-status.md) et définissez le membre **dwItem** de la structure d' [**\_ état \_ MCI**](mci-status-parms.md) sur le tempo d’état de MCI \_ Seq \_ \_ . Si la commande d' **\_ État MCI** est réussie, le membre **dwReturn** de la structure d' **\_ \_ État MCI** contient le tempo en cours.

Pour modifier le tempo, utilisez la commande [**MCI \_ Set**](mci-set.md) avec la structure [**MCI \_ Seq \_ Set \_ PARMS**](mci-seq-set-parms.md) , en spécifiant l' \_ indicateur de tempo du paramètre MCI Seq \_ \_ et en définissant le tempo souhaité dans le membre **dwTempo** de la structure.

La façon dont le tempo est représenté dépend du type de division de la séquence. Si le type de division est PPQN, le tempo est représenté en temps par minute. Si le type de division est l’un des types de division SMPTE, le tempo est représenté en images par seconde. Pour plus d’informations sur la détermination du type de division d’une séquence, consultez [récupération du type de division de séquence](retrieving-the-sequence-division-type.md).

 

 




