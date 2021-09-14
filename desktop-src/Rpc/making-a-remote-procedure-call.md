---
title: Exécution d’un appel de procédure distante
description: Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Appel de procédure distante RPC, tâches, appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194100"
---
# <a name="making-a-remote-procedure-call"></a>Exécution d’un appel de procédure distante

Une fois que le programme client des applications distribuées qui utilise des handles de liaison explicites a un handle de liaison, il peut exécuter des procédures distantes.

Microsoft RPC offre également des handles de liaison personnalisés, des handles de liaison implicites et des handles de liaison automatiques. Ces handles de liaison offrent aux programmes clients et serveurs différents différents niveaux de contrôle sur le processus d’exécution des procédures distantes. Pour plus d’informations sur les différents types de handle et la flexibilité qu’ils offrent, consultez [liaison et Handles](binding-and-handles.md).

Pour exécuter l’appel de procédure à distance, appelez la fonction stub côté client de la même manière que n’importe quelle fonction C est appelée.

 

 




