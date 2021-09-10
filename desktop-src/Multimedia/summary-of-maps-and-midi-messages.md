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
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364539"
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

 

 




