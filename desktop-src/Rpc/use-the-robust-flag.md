---
title: Utiliser l’indicateur/Robust
description: Compilez toujours les fichiers. idl à l’aide du commutateur/Robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941130"
---
# <a name="use-the-robust-flag"></a>Utiliser l’indicateur/Robust

Compilez toujours les fichiers. idl à l’aide du commutateur [**/Robust**](/windows/desktop/Midl/-robust) . L’utilisation du commutateur **/Robust** génère des informations supplémentaires qui permettent au moteur de représentation de données réseau d’effectuer une vérification des erreurs au moment de l’exécution sur des arguments corrélés dans des tableaux dynamiques, des unions et des pointeurs d’interface out dans des applications com et RPC. Si le logiciel ne peut pas être compilé avec cet indicateur, le logiciel est tellement exposé à des attaques qu’aucun effort dans une autre zone ne peut protéger.

 

 