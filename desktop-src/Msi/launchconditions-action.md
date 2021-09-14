---
description: L’action LaunchConditions interroge la table LaunchCondition et évalue chaque instruction conditionnelle enregistrée ici. Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Action LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011979"
---
# <a name="launchconditions-action"></a>Action LaunchConditions

L’action LaunchConditions interroge la [table LaunchCondition](launchcondition-table.md) et évalue chaque instruction conditionnelle enregistrée ici. Si l’une de ces instructions conditionnelles échoue, un message d’erreur s’affiche pour l’utilisateur et l’installation est interrompue.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action LaunchConditions est facultative. Cette action est normalement la première dans la séquence, mais l' [action AppSearch](appsearch-action.md) peut être séquencée avant l’action LaunchConditions. Si des conditions de lancement ne s’appliquent pas à tous les modes d’installation, la propriété du mode d’installation appropriée doit être utilisée dans une expression conditionnelle dans la table de séquences appropriée.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

 

 



