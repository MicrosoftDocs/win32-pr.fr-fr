---
title: Conseils de migration
description: Il est important de prendre en compte les calculs d’adresses et les opérations arithmétiques de pointeur lors du Portage de votre code vers le Windows 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- guide de programmation Windows 64 bits 64-bits Windows programmation, conseils de migration
- conseils de migration 64-programmation de Windows bits
- compatibilité 64 bits-programmation Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743594"
---
# <a name="migration-tips"></a>Conseils de migration

Les deux principaux points à se poser lors de l’examen de votre code pour la compatibilité 64 bits sont les suivants :

-   Calculs d’adresses
-   Arithmétique des pointeurs

Pour de nombreuses raisons, les développeurs ont des adresses stockées en tant que valeur **ULong** . après tout, sur l’Windows 32 bits, une adresse, un pointeur et une valeur **ULONG** sont tous les 32 bits de long. toutefois, sur les Windows 64 bits, une adresse et un **ULONG** ne sont pas de la même longueur. Alors qu’un **ULong** reste une valeur 32 bits, tous les pointeurs sont maintenant des valeurs de 64 bits.

## <a name="in-this-section"></a>Dans cette section

-   [Instructions générales sur le portage](general-porting-guidelines.md)
-   [Stockage d’une valeur 64 bits](storing-a-64-bit-value.md)
-   [Erreurs courantes du compilateur](common-compiler-errors.md)
-   [Considérations supplémentaires](additional-considerations.md)

 

 




