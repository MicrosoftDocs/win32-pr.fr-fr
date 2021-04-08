---
title: Conseils de migration
description: Il est important de prendre en compte les calculs d’adresses et les opérations arithmétiques de pointeur lors du Portage de votre code vers Windows 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, conseils sur la migration
- conseils de migration 64 bits de la programmation Windows
- compatibilité avec la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674006"
---
# <a name="migration-tips"></a>Conseils de migration

Les deux principaux points à se poser lors de l’examen de votre code pour la compatibilité 64 bits sont les suivants :

-   Calculs d’adresses
-   Arithmétique des pointeurs

Pour de nombreuses raisons, les développeurs ont des adresses stockées en tant que valeur **ULong** . Après tout, sur Windows 32 bits, une adresse, un pointeur et une valeur **ULong** sont tous les 32 bits de long. Toutefois, sur Windows 64 bits, une adresse et un **ULong** ne sont pas de la même longueur. Alors qu’un **ULong** reste une valeur 32 bits, tous les pointeurs sont maintenant des valeurs de 64 bits.

## <a name="in-this-section"></a>Dans cette section

-   [Instructions générales sur le portage](general-porting-guidelines.md)
-   [Stockage d’une valeur 64 bits](storing-a-64-bit-value.md)
-   [Erreurs courantes du compilateur](common-compiler-errors.md)
-   [Considérations supplémentaires](additional-considerations.md)

 

 




