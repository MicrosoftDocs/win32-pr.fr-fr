---
description: Le Service VSS (VSS) est un ensemble d’API COM et C++ qui permettent d’effectuer des sauvegardes de volume alors que les applications sur le système (appelées rédacteurs) continuent d’écrire sur les volumes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Informations de référence sur l’API de cliché instantané de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbc2d0bec6d68572a67a1dc80327fb80028d7f8d98487f24fec24e2c2e65f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751526"
---
# <a name="volume-shadow-copy-api-reference"></a>Informations de référence sur l’API de cliché instantané de volume

Le Service VSS (VSS) est un ensemble d’API COM et C++ qui permettent d’effectuer des sauvegardes de volume alors que les applications sur le système (appelées rédacteurs) continuent d’écrire sur les volumes.

VSS prend en charge ces sauvegardes par le biais de la création de clichés instantanés, un doublon du volume d’origine à un moment donné.

Les développeurs tiers peuvent utiliser l’API VSS pour créer des demandeurs (par exemple, une application de sauvegarde) pour créer et gérer des clichés instantanés.

Le travail réel de création et de représentation des clichés instantanés est effectué par les applications de niveau système appelées fournisseurs.

Les développeurs peuvent également utiliser l’API pour construire des enregistreurs : les applications prenant en charge VSS, capables de coordonner les opérations d’e/s avec la création et la manipulation de clichés instantanés.

-   [Classes d’API de cliché instantané du volume](volume-shadow-copy-api-classes.md)
-   [Types de données de l’API de cliché instantané des volumes](volume-shadow-copy-api-data-types.md)
-   [Énumérations de l’API de cliché instantané du volume](volume-shadow-copy-api-enumeration-types.md)
-   [Fonctions de l’API de cliché instantané du volume](volume-shadow-copy-api-functions.md)
-   [Interfaces API du cliché instantané du volume](volume-shadow-copy-api-interfaces.md)
-   [Structures de l’API de cliché instantané des volumes](volume-shadow-copy-api-structures.md)
-   [Glossaire des clichés instantanés de volume](volume-shadow-copy-glossary.md)

Pour plus d’informations sur l’écriture des demandeurs et des writers, consultez [utilisation de l’service VSS](using-the-volume-shadow-copy-service.md).

 

 



