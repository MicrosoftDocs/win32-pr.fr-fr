---
title: Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte
description: Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671274"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>Octroi du droit d’ouverture de session en tant que service sur l’ordinateur hôte

Lors de l’installation d’un service pour qu’il s’exécute sous un compte d’utilisateur de domaine, le compte doit disposer du droit d’ouvrir une session en tant que service sur l’ordinateur local. N’oubliez pas que ce droit d’ouverture de session s’applique uniquement à l’ordinateur local et doit être accordé dans la stratégie LSA locale de chaque ordinateur hôte. Cette étape n’est pas requise si votre service s’exécute en tant que LocalSystem, qui, par défaut, reçoit ce droit.

Pour plus d’informations sur la façon d’accorder un droit d’ouverture de session en tant que service par programmation, consultez l' [exemple de code LSAPrivs](https://www.google.com/#q=LSAPrivs).

 

 




