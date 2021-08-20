---
title: résumé des Messages Cartes et MIDI
description: résumé des Messages Cartes et MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- L’interface MIDI (Musical Instrument Digital Interface), le Mappeur MIDI
- MIDI (Musical Instrument Digital Interface), Mappeur MIDI
- Mappeur MIDI, mappage de canal
- Mappeur MIDI, mappages de correctifs
- Mappeur MIDI, mappages de clés
- carte de canal
- mappages de correctifs
- cartes clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89c23d6326e19cb5680906155d5ee2e8dbcc32735fabd8625658410ef4ddfa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781849"
---
# <a name="summary-of-maps-and-midi-messages"></a>résumé des Messages Cartes et MIDI

Voici les octets d’État pour les messages MIDI et les types de cartes qui affectent chaque message.



| État MIDI | Description               | Types de cartes                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Note désactivée                  | Cartes de canaux, cartes clés   |
| 0x90-0x9F   | Remarque sur                    | Cartes de canaux, cartes clés   |
| 0xA0-0xAF   | Polyphonic-clé aftertouch | Cartes de canaux, cartes clés   |
| 0xB0-0xBF   | Modification du contrôle            | Cartes de canaux, mappages de correctifs |
| 0xC0-0xCF   | Changement de programme            | Cartes de canaux, mappages de correctifs |
| 0xD0-0xDF   | Canal aftertouch        | Cartes de canal             |
| 0xE0-0xEF   | Changement de courbure         | Cartes de canal             |
| 0xF0-0xFF   | Système                    | Non mappé               |



 

-   Les quatre bits de poids fort représentent la valeur d’État. Les quatre bits de poids faible représentent les informations de canal.
-   Les mappages de correctifs affectent uniquement le contrôleur 7 (volume principal).
-   Les messages système sont envoyés à tous les appareils répertoriés dans une carte de canal.

 

 




