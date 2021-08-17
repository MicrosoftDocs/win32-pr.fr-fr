---
description: Si la fonction de rappel par défaut va être appelée au cours de l’engagement de la file d’attente, le contexte de celle-ci doit être initialisé à l’aide des fonctions SetupInitDefaultQueueCallback ou SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Validation de la file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67c19b91cc25e5107f91fbd241d96147137a38b8544568e57ea3bbbd58981a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887520"
---
# <a name="committing-the-queue"></a>Validation de la file d’attente

Si la fonction de rappel par défaut va être appelée au cours de l’engagement de la file d’attente, le contexte de celle-ci doit être initialisé à l’aide des fonctions [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) . Si vous utilisez une fonction de rappel personnalisée qui n’appelle jamais la fonction de rappel par défaut, cette étape n’est pas nécessaire.

Une fois la file d’attente générée et la fonction de rappel qui traite les notifications de file d’attente a été initialisée, vous pouvez appeler [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour valider les opérations qui ont été mises en file d’attente.

L’exemple suivant utilise [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) pour valider la file d’attente à l’aide de la routine de rappel par défaut.

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

Dans l’exemple précédent, MyQueue est la file d’attente à valider, OwnerWindow est la fenêtre qui possède toutes les boîtes de dialogue créées par la routine de rappel par défaut, SetupDefaultQueueCallback spécifie que la fonction de rappel par défaut sera utilisée, et *Context* est un pointeur vers la structure retournée par l’appel précédent à [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).

 

 



