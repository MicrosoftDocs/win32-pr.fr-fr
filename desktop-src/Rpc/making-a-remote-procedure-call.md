---
title: Exécution d’un appel de procédure distante
description: Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Appel de procédure distante RPC, tâches, appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020079"
---
# <a name="making-a-remote-procedure-call"></a>Exécution d’un appel de procédure distante

Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.

Microsoft RPC offre également des handles de liaison personnalisés, des handles de liaison implicites et des handles de liaison automatiques. Ces handles de liaison offrent aux programmes clients et serveurs différents différents niveaux de contrôle sur le processus d’exécution des procédures distantes. Pour plus d’informations sur les différents types de handle et la flexibilité qu’ils offrent, consultez [liaison et Handles](binding-and-handles.md).

Pour exécuter l’appel de procédure à distance, appelez la fonction stub côté client de la même manière que n’importe quelle fonction C est appelée.

 

 




