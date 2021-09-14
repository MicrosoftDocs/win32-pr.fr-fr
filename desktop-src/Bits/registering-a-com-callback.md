---
title: Inscription d’un rappel COM
description: Au lieu d’interroger les modifications de l’état d’un travail, vous pouvez vous inscrire pour recevoir une notification en cas de modification de l’état du travail.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- BITS de tâche de transfert, notification d’événement
- inscription pour les BITS de notification d’événements
- BITS de notification d’événement
- BITS de notification d’événements, rappels
- BITS des événements de notification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126924403"
---
# <a name="registering-a-com-callback"></a>Inscription d’un rappel COM

Au lieu d' [interroger](polling-for-the-status-of-the-job.md) les modifications de l’état d’un travail, vous pouvez vous inscrire pour recevoir une notification en cas de modification de l’état du travail. Pour recevoir une notification, vous devez implémenter l’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) . L’interface contient les méthodes suivantes que BITS appelle, en fonction de votre inscription :

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Pour obtenir un exemple qui implémente l’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , consultez l’exemple de code dans la rubrique de l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .

L’interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fournit une notification lorsqu’un fichier est transféré. En général, vous utilisez cette méthode pour valider le fichier, afin que le fichier soit disponible pour le téléchargement des homologues. dans le cas contraire, le fichier n’est pas disponible pour les homologues tant que vous n’appelez pas la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Pour valider le fichier, appelez la méthode [**IBackgroundCopyFile3 :: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .

Il existe deux méthodes pour inscrire un rappel COM : l’inscription d’un objet de rappel ou l’inscription d’un ID de classe de rappel. L’utilisation d’un objet de rappel est plus simple et moins lourde. l’utilisation d’un CLSID de rappel est plus fiable, mais plus complexe. Vous pouvez inscrire l’un ou l’autre, ou aucun des deux : BITS utilisera un objet de rappel s’il en existe un et peut encore être appelé, et reviendra à l’instanciation d’un nouvel objet basé sur un ID de classe fourni si cette opération échoue.

### <a name="registering-a-callback-object"></a>Inscription d’un objet de rappel

Pour inscrire votre implémentation avec BITS, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) . Pour spécifier les méthodes que BITS appelle, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).

L’interface de notification n’est plus valide quand votre application se termine ; BITS ne rend pas persistant l’interface Notify. Par conséquent, le processus d’initialisation de votre application doit enregistrer les tâches existantes pour lesquelles vous souhaitez recevoir des notifications. Si vous avez besoin de capturer l’État et les informations de progression qui se sont produites depuis la dernière exécution de votre application, interrogez les informations d’État et de progression pendant l’initialisation de l’application.

Avant de quitter, votre application doit effacer le pointeur d’interface de rappel (**SetNotifyInterface (null)**). Il est plus efficace d’effacer le pointeur de rappel que de laisser les BITS découvrir qu’il n’est plus valide.

Notez que si plusieurs applications appellent la méthode [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) pour définir l’interface de notification pour le travail, la dernière application à appeler la méthode **SetNotifyInterface** est celle qui recevra les notifications ; les autres applications ne recevront pas de notifications.

L’exemple suivant montre comment s’inscrire pour les notifications. L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide. Pour plus d’informations sur l’exemple de classe CNotifyInterface utilisé dans l’exemple suivant, consultez l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a>Inscription d’un CLSID de rappel

Pour inscrire un CLSID de rappel avec BITS, appelez la méthode [**IBackgroundCopyJob5 :: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) avec l' **\_ \_ \_ \_ identificateur de propriété de la tâche bits** PropertyId. Pour spécifier les méthodes que BITS appelle, appelez la méthode [**méthode ibackgroundcopyjob :: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .

Vous devez vous assurer que le CLSID de notification est inscrit sur un serveur COM hors processus avant d’inscrire le CLSID avec un travail BITS. L’implémentation d’un [serveur com](/windows/desktop/com/com-server-responsibilities) est beaucoup plus compliquée que la définition et la transmission d’un objet de rappel, mais offre plusieurs avantages importants. Un serveur COM permet à BITS de maintenir l’association entre un travail BITS et le code de votre application entre les redémarrages du système et les tâches de longue durée ou durables. Un serveur COM permet également à votre application de s’arrêter complètement alors que BITS continue d’exécuter les transferts en arrière-plan, ce qui peut améliorer l’utilisation de la batterie, du processeur et de la mémoire du système.

Pour fournir une notification que vous avez enregistrée pour la réception, BITS tente d’abord d’appeler la méthode correspondante d’un objet de rappel existant que vous avez peut-être attaché. S’il n’existe aucun objet, ou si cet objet existant a été déconnecté (généralement suite à l’arrêt de votre application), BITS appelle CoCreateInstance en utilisant le CLSID de notification pour instancier un nouvel objet de rappel et utilise cet objet pour tous les rappels ultérieurs jusqu’à ce qu’il soit déconnecté ou remplacé par un nouvel appel à [**méthode ibackgroundcopyjob :: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).

Contrairement aux objets de rappel, le CLSID de rappel est conservé avec leurs travaux BITS correspondants si le service BITS ou le système sont arrêtés et redémarrés. Votre application peut effacer tout CLSID de notification précédemment défini avant de quitter (ou à tout autre moment) en passant un nouveau CLSID de notification de GUID \_ null, mais votre application peut préférer laisser le CLSID de notification inscrit si votre application s’est inscrite pour que com la démarre en réponse à des demandes CoCreateInstance pour votre CLSID. Notez que si plusieurs applications définissent les appels à la propriété **CLSID de notification de \_ propriété de tâche \_ \_ \_ bits** , le dernier CLSID à définir est celui utilisé par bits pour instancier les objets de rappel. les autres CLSID ne seront pas instanciés. De même, si une application inscrit un CLSID et qu’un autre inscrit un objet de rappel, les règles habituelles pour l’objet de rappel qui prend la priorité s’appliquent et le CLSID n’est pas utilisé à moins que l’objet de rappel soit effacé ou déconnecté.

L’exemple suivant montre comment s’inscrire pour les notifications CLSID. L’exemple suppose que le pointeur d’interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) est valide et que votre application est déjà inscrite en tant que serveur com hors processus qui implémente la classe CNotifyInterface. Pour plus d’informations sur l’exemple de classe CNotifyInterface utilisé dans l’exemple suivant, consultez l’interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 