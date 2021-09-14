---
description: Les lecteurs sont des appareils standard dans un système de carte à puce. Ils sont contrôlés par des pilotes et sont introduits et supprimés du système via Plug-and-Play ou via l’élément périphériques du panneau de configuration.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lecteurs de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324768"
---
# <a name="smart-card-readers"></a>Lecteurs de carte à puce

Les lecteurs sont des appareils standard dans un système de [*carte à puce*](../secgloss/s-gly.md) . Ils sont contrôlés par des pilotes et sont introduits et supprimés du système via Plug-and-Play ou via l’élément périphériques du panneau de configuration.

Chaque lecteur doit être défini pour être utilisé par le [*sous-système de carte à puce*](../secgloss/s-gly.md). Le sous-système n’est pas responsable des lecteurs qui ne lui sont pas spécifiquement attribués.

Les lecteurs de carte à puce peuvent être divisés en groupes logiques appelés groupes de lecteurs. Ces groupes peuvent être définis par le sous-système, ainsi que par les administrateurs et les utilisateurs. Un lecteur peut appartenir à plusieurs groupes de lecteurs

Le sous-système de carte à puce définit les groupes suivants.



| Groupe                | Description                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cicatrice $ AllReaders     | Ce groupe contient tous les lecteurs du système. Un nouveau lecteur donné au sous-système de la carte à puce est automatiquement inclus dans le groupe de lecteurs à l’ensemble du système, à raison d’un cicatrice $ AllReaders.                         |
| Cicatrice $ DefaultReaders | Ce groupe par défaut, un pour chaque [*Terminal*](../secgloss/t-gly.md), contient tous les lecteurs attribués au terminal et qui ne sont pas réservés à une utilisation spécifique. |



 

 

 
