---
description: En utilisant le sous-système de carte à puce, vous pouvez communiquer avec des cartes qui peuvent ne pas se conformer aux spécifications ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Fonctions d’accès direct aux cartes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861985"
---
# <a name="direct-card-access-functions"></a>Fonctions d’accès direct aux cartes

En utilisant le sous-système de [*carte à puce*](/windows/desktop/SecGloss/s-gly) , vous pouvez communiquer avec des cartes qui peuvent ne pas se conformer aux spécifications ISO 7816. Pour ce faire, les fonctions suivantes vous permettent de contrôler les attributs des communications entre l’application et la carte en vous donnant une manipulation directe et de bas niveau du [*lecteur*](/windows/desktop/SecGloss/r-gly).

Pour utiliser ces fonctions, vous devez fournir un identificateur pour l’attribut en question. Pour obtenir des identificateurs et des valeurs d’attributs valides, consultez la table 3-1 dans *Requirements for PC-Connected Interface Devices*.



| Rubrique                                    | Description                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Fournissez un contrôle direct du lecteur. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obtient les attributs de lecteur.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Définissez l’attribut Reader.                 |



 

 

 
