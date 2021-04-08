---
title: Prise en charge des pilotes pour les commandes MCI
description: Prise en charge des pilotes pour les commandes MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672590"
---
# <a name="driver-support-for-mci-commands"></a>Prise en charge des pilotes pour les commandes MCI

Les pilotes MCI fournissent les fonctionnalités pour les commandes MCI. Le logiciel système effectue des tâches de gestion de données de base, mais l’ensemble de la lecture, de la présentation et de l’enregistrement multimédia est géré par les pilotes MCI individuels.

Les pilotes varient en fonction de la prise en charge des commandes MCI et des indicateurs de commande. Étant donné que les périphériques multimédias peuvent avoir des fonctionnalités très différentes, MCI est conçu pour permettre aux pilotes individuels d’étendre ou de réduire les jeux de commandes pour qu’ils correspondent aux fonctionnalités de l’appareil. Par exemple, la commande d' [**enregistrement**](record.md) ([**\_ enregistrement MCI**](mci-record.md)) fait partie du jeu de commandes pour les séquenceurs midi, mais le pilote MCISEQ inclus avec Windows ne prend pas en charge cette commande. La rubrique de référence pour la commande record explique que les appareils du type d’appareil **Sequencer** reconnaissent la commande ; Cela ne signifie pas que tous les appareils de ce type prennent en charge la commande. Les applications doivent utiliser la commande [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) pour déterminer les capacités d’un appareil particulier.

 

 




