---
description: L’action LaunchConditions interroge la table LaunchCondition et évalue chaque instruction conditionnelle enregistrée ici. Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Action LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a973e6e1de81091039de12e07e8edb890c860e5be54e942f00406e39e62e229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086029"
---
# <a name="launchconditions-action"></a>Action LaunchConditions

L’action LaunchConditions interroge la [table LaunchCondition](launchcondition-table.md) et évalue chaque instruction conditionnelle enregistrée ici. Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action LaunchConditions est facultative. Cette action est normalement la première dans la séquence, mais l' [action AppSearch](appsearch-action.md) peut être séquencée avant l’action LaunchConditions. Si des conditions de lancement ne s’appliquent pas à tous les modes d’installation, la propriété du mode d’installation appropriée doit être utilisée dans une expression conditionnelle dans la table de séquences appropriée.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

 

 



