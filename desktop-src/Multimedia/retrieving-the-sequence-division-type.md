---
title: Récupération du type de division de séquence
description: Récupération du type de division de séquence
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (Musical Instrument Digital Interface), type de division de séquence
- MIDI (Musical Instrument Digital Interface), type de division de séquence
- Séquenceur MIDI MCI, type de division
- Commande MCI_STATUS
- type de division de séquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801803"
---
# <a name="retrieving-the-sequence-division-type"></a>Récupération du type de division de séquence

Le *type de division* d’une séquence MIDI détermine la durée entre les événements midi de la séquence. Pour déterminer le type de division d’une séquence, utilisez la commande [**MCI \_ Status**](mci-status.md) et définissez le membre **dwItem** de la structure de l' [**\_ état \_ MCI**](mci-status-parms.md) sur MCI \_ Seq \_ Status \_ DIVTYPE.

Si la commande d' **\_ État MCI** est réussie, le membre **dwReturn** de la structure d' **\_ \_ État MCI** contient l’une des valeurs suivantes pour indiquer le type de division.



| Valeur                        | Type de division                     |
|------------------------------|-----------------------------------|
| MCI \_ Seq \_ div \_ PPQN          | PPQN (note de pièces par trimestre)     |
| MCI \_ Seq \_ div \_ SMPTE \_ 24     | SMPTE, 24 fps (images par seconde) |
| MCI \_ Seq \_ div \_ SMPTE \_ 25     | SMPTE, 25 i/s                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30     | SMPTE, 30 i/s                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30DROP | SMPTE, trame de dépôt de 30 i/s          |



 

Vous devez connaître le type de division d’une séquence à modifier ou interroger son tempo. Vous ne pouvez pas modifier le type de division d’une séquence à l’aide du séquenceur MCI.

 

 




