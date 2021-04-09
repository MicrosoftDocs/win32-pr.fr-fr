---
description: La table CounterData contient une ligne pour chaque compteur qui est collecté à un moment donné. Il y aura un grand nombre de ces lignes.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865126"
---
# <a name="counterdata"></a>CounterData

La table **CounterData** contient une ligne pour chaque compteur qui est collecté à un moment donné. Il y aura un grand nombre de ces lignes.

La table **CounterData** définit les champs suivants :

-   **GUID :** GUID de ce jeu de données. Utilisez cette clé pour joindre la table [**DisplayToID**](displaytoid.md) .
-   **CounterID :** Identifie le compteur. Utilisez cette clé pour joindre la table [**CounterDetails**](counterdetails.md) .
-   **RecordIndex :** L’exemple d’index pour un identificateur de compteur et un GUID de collection spécifiques. La valeur augmente pour chaque échantillon successif dans ce fichier journal.
-   **CounterDateTime :** Heure à laquelle la collection a été démarrée, en heure UTC.
-   **CounterValue :** Valeur mise en forme du compteur. Cette valeur peut être égale à zéro pour le premier enregistrement si le compteur requiert deux exemples pour calculer une valeur affichable.
-   **FirstValueA :** Associez cette valeur 32 bits à la valeur de **FirstValueB** pour créer le membre **FirstValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA** contient les bits de poids faible.
-   **FirstValueB :** Associez cette valeur 32 bits à la valeur de **FirstValueA** pour créer le membre **FirstValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB** contient les bits de poids fort.
-   **SecondValueA :** Associez cette valeur 32 bits à la valeur de **SecondValueB** pour créer le membre **SecondValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contient les bits de poids faible.
-   **SecondValueB :** Associez cette valeur 32 bits à la valeur de **SecondValueA** pour créer le membre **SecondValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contient les bits de poids fort.

Les champs **GUID**, **CounterID** et **RecordIndex** constituent la clé primaire de cette table.

 

 



