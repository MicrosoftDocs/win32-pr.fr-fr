---
description: Définition du journal des erreurs
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Définition du journal des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d28c337d146927ee624dad6f350d163e4bde3756acaf6fb0418821cc7ac5c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904199"
---
# <a name="setting-the-error-log"></a>Définition du journal des erreurs

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Après avoir implémenté la classe de journalisation des erreurs, créez une nouvelle instance de la classe. ensuite, donnez à [DirectShow Services de modification](directshow-editing-services.md) un pointeur en appelant la méthode [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie. Interrogez la chronologie de l’interface **IAMSetErrorLog** . Pour vous assurer que toutes les erreurs sont journalisées, vous devez appeler cette méthode avant de charger, d’enregistrer ou de rendre la chronologie.


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



La journalisation des erreurs n’a aucun effet sur les valeurs de retour que vous recevez lorsque vous appelez des méthodes dans votre application. La journalisation des erreurs complète, mais ne remplace pas les techniques de gestion des erreurs habituelles. Pour créer une application robuste, vérifiez toujours les valeurs HRESULT.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation des erreurs](logging-errors.md)
</dt> </dl>

 

 



