---
title: Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte
description: Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188953"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte

Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local. N’oubliez pas que ce droit d’ouverture de session s’applique uniquement à l’ordinateur local et doit être accordé dans la stratégie LSA locale de chaque ordinateur hôte. Cette étape n’est pas requise si votre service s’exécute en tant que LocalSystem, qui, par défaut, reçoit ce droit.

Pour plus d’informations sur la façon d’accorder un droit d’ouverture de session en tant que service par programmation, consultez l' [exemple de code LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




