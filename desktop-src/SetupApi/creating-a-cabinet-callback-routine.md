---
description: Étant donné que l’API d’installation ne fournit pas de routine de rappel d’armoire par défaut, vous devez fournir une routine. La routine de rappel requise par la fonction SetupIterateCabinet doit avoir la même forme que celle vers laquelle pointe FileCallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Création d’une routine de rappel d’armoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203174"
---
# <a name="creating-a-cabinet-callback-routine"></a>Création d’une routine de rappel d’armoire

Étant donné que l’API d’installation ne fournit pas de routine de rappel d’armoire par défaut, vous devez fournir une routine. La routine de rappel requise par la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) doit avoir la même forme que celle vers laquelle pointe [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).

Voici la syntaxe utilisée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour envoyer une notification à la routine de rappel.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Le paramètre de *contexte* est un pointeur void vers une structure ou une variable de contexte qui peut être utilisée par la routine de rappel pour stocker des informations qui doivent être conservées entre les appels suivants de la routine de rappel.

L’implémentation de ce contexte est spécifiée par la routine de rappel et n’est jamais référencée ou modifiée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

Le paramètre de *notification* est un entier non signé et sera l’une des valeurs suivantes.



| Notification                                                        | Description                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | Le fichier a été extrait de l’armoire.      |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | Un fichier est trouvé dans le fichier CAB.              |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | Le fichier actuel se poursuit dans le fichier CAB suivant. |



 

Les deux derniers paramètres, *param1* et *param2*, sont également des entiers non signés et contiennent des informations supplémentaires relatives à la notification. Pour plus d’informations sur les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consultez [notifications de fichier CAB](cabinet-file-notifications.md).

Une \_ routine de rappel de notification de fichier SP \_ \_ retourne un entier non signé. La routine de rappel du fichier cab doit retourner l’une des valeurs suivantes en fonction de la notification.

Pour la \_ notification SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) s’attend à ce que l’une des valeurs suivantes soit retournée par la routine de rappel.



| Valeur         | Signification                   |
|---------------|---------------------------|
| \_abandon FILEOP | Abandon du traitement du fichier CAB. |
| FILEOP \_ doit  | Extrayez le fichier actif. |
| FILEOP \_ Ignorer  | Ignore le fichier actuel.    |



 

Pour les \_ notifications SPFILENOTIFY NEEDNEWCABINET et SPFILENOTIFY \_ FILEEXTRACTED, **SetupIterateCabinet** s’attend à ce que l’une des valeurs suivantes soit retournée par la routine de rappel.



| Valeur      | Signification                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUCUNE \_ erreur  | Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.                                                                                                                                                                        |
| ERREUR \_ xxx | Une erreur du type spécifié s’est produite. La fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la **valeur false** et le code d’erreur spécifié est retourné par un appel à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). |



 

Si la routine de rappel retourne FILEOP \_ doit, la routine doit également fournir un chemin d’accès cible complet. Pour plus d’informations, consultez [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).

 

 
