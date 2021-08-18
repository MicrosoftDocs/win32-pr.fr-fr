---
description: les séquences d’échappement fournies par le Windows 16 bits permettaient d’accéder aux fonctionnalités spéciales des appareils.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Échappements de l’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711559"
---
# <a name="printer-escapes"></a>Échappements de l’imprimante

les séquences d’échappement fournies par le Windows 16 bits permettaient d’accéder aux fonctionnalités spéciales des appareils. la plupart de ces séquences d’échappement sont obsolètes, mais quelques-unes sont fournies pour simplifier le portage des applications Windows 16 bits. GDI prend en charge un ensemble complet de fonctions de chemin d’accès que les applications peuvent utiliser à la place des séquences d’échappement pour dessiner des chemins d’accès sur n’importe quel appareil. Pour obtenir la liste des fonctions qui remplacent certaines séquences d’échappement, consultez la fonction [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

Des séquences d’échappement d’imprimante 64 d’origine, seuls **QUERYESCSUPPORT** et **passthrough** peuvent être utilisés.

Il existe également une fonction d’échappement étendue appelée [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Cette fonction permet aux applications d’accéder aux fonctionnalités d’un appareil particulier qui ne sont pas directement disponibles via GDI.

 

 



