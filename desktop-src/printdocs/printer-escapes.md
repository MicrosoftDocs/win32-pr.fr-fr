---
description: Les séquences d’échappement fournies par Windows 16 bits ont permis l’accès aux fonctionnalités spéciales de l’appareil.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Échappements de l’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203469"
---
# <a name="printer-escapes"></a>Échappements de l’imprimante

Les séquences d’échappement fournies par Windows 16 bits ont permis l’accès aux fonctionnalités spéciales de l’appareil. La plupart de ces séquences d’échappement sont obsolètes, mais quelques-unes sont fournies pour simplifier le portage des applications Windows 16 bits. GDI prend en charge un ensemble complet de fonctions de chemin d’accès que les applications peuvent utiliser à la place des séquences d’échappement pour dessiner des chemins d’accès sur n’importe quel appareil. Pour obtenir la liste des fonctions qui remplacent certaines séquences d’échappement, consultez la fonction [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

Des séquences d’échappement d’imprimante 64 d’origine, seuls **QUERYESCSUPPORT** et **passthrough** peuvent être utilisés.

Il existe également une fonction d’échappement étendue appelée [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Cette fonction permet aux applications d’accéder aux fonctionnalités d’un appareil particulier qui ne sont pas directement disponibles via GDI.

 

 



