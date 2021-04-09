---
description: Une fois que vous avez obtenu un handle vers une file d’attente de fichiers en appelant la fonction SetupOpenFileQueue, vous pouvez ajouter des opérations de fichier à la file d’attente, soit fichier par fichier, soit en mettant en file d’attente tous les fichiers dans une section INF.
ms.assetid: ba2f40cd-b0df-4768-8080-4fd80c50f2c2
title: Mise en file d’attente des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5ab9a9be136e50547076c8daf9bd519ade72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865421"
---
# <a name="queuing-files"></a>Mise en file d’attente des fichiers

Une fois que vous avez obtenu un handle vers une file d’attente de fichiers en appelant la fonction [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) , vous pouvez ajouter des opérations de fichier à la file d’attente, soit fichier par fichier, soit en mettant en file d’attente tous les fichiers dans une section INF.

Pour ajouter une opération de copie pour un fichier individuel à la file d’attente de fichiers, appelez la fonction [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya) . Si vous souhaitez placer en file d’attente une opération de copie de fichiers à l’aide du média source par défaut et des destinations cibles spécifiées dans un fichier INF, vous pouvez appeler la fonction [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya) .

Vous pouvez ajouter une opération de suppression ou de modification de nom de fichier à la file d’attente ouverte, en appelant la fonction [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) ou [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea) .

 

 



