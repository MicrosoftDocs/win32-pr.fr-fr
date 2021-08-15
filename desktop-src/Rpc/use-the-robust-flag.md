---
title: Utiliser l’indicateur/Robust
description: Compilez toujours les fichiers. idl à l’aide du commutateur/Robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010887"
---
# <a name="use-the-robust-flag"></a>Utiliser l’indicateur/Robust

Compilez toujours les fichiers. idl à l’aide du commutateur [**/Robust**](/windows/desktop/Midl/-robust) . L’utilisation du commutateur **/Robust** génère des informations supplémentaires qui permettent au moteur de représentation de données réseau d’effectuer une vérification des erreurs au moment de l’exécution sur des arguments corrélés dans des tableaux dynamiques, des unions et des pointeurs d’interface out dans des applications com et RPC. Si le logiciel ne peut pas être compilé avec cet indicateur, le logiciel est tellement exposé à des attaques qu’aucun effort dans une autre zone ne peut protéger.

 

 