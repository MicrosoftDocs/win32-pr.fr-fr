---
title: Clés et entrées de Registre pour un magasin de type 2 en ligne
description: Clés et entrées de Registre pour un magasin de type 2 en ligne
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Lecteur Windows Media magasins en ligne, registre
- magasins en ligne, registre
- type 2 magasins en ligne, registre
- Registre, type 2 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416209"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Clés et entrées de Registre pour un magasin de type 2 en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

pour rendre disponible un magasin en ligne de type 2 dans Lecteur Windows Media, le fournisseur de magasin en ligne doit créer les sous-clés et les entrées de registre suivantes sur l’ordinateur de l’utilisateur.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au magasin en ligne. Le tableau suivant décrit ces espaces réservés.



| Espace réservé    | Description                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Chaîne convenue entre Microsoft et le magasin en ligne. Cette chaîne identifie de façon unique le magasin en ligne. Exemple : « Proseware »<br/>                                                                                                                                                                                                                                                          |
| *flags*        | un or **au niveau du** bit d’une ou de plusieurs fonctionnalités de plug-in signalent que ces indicateurs spécifient si Lecteur Windows Media doit appeler des méthodes particulières de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) et [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2). Pour plus d’informations sur les indicateurs pris en charge, consultez le tableau des indicateurs de capacité de plug-in qui suit ce tableau. Exemple : 00000037<br/> |
| *identificateur*        | GUID qui est l’identificateur de classe (CLSID) de la classe qui implémente **IWMPSubscriptionService** dans le plug-in du magasin en ligne. Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *convivial* | Nom convivial du magasin en ligne. exemple : « proseware Musique Service »<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Nom du plug-in du magasin en ligne. Exemple : « plug-in de service Proseware »<br/>                                                                                                                                                                                                                                                                                                                  |
| *ClassName*    | Nom de la classe qui implémente **IWMPSubscriptionService** dans le plug-in du magasin en ligne. Exemple : « CProsewareService »<br/>                                                                                                                                                                                                                                                                |
| *NomModule*   | Chemin d’accès complet à la DLL qui implémente le plug-in du magasin en ligne. Exemple : « C : \\ Program Files \\ proseware \\ProsewareService.dll »<br/>                                                                                                                                                                                                                                                |



 

Le tableau suivant décrit les indicateurs de capacité de plug-in.



| Indicateur                                    | Valeur | Description                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| limite d’abonnement \_ \_ ALLOWPLAY            | 0X1   | Lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| limite d’abonnement \_ \_ ALLOWCDBURN          | 0X2   | Lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| limite d’abonnement \_ \_ ALLOWPDATRANSFER     | 0X4   | Lecteur Windows Media doit appeler [IWMPSubscriptionService :: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| limite d’abonnement \_ \_ BACKGROUNDPROCESSING | 0X8   | Lecteur Windows Media doit appeler [IWMPSubscriptionService :: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| limite d’abonnement \_ \_ DEVICEAVAILABLE      | 0X10  | Lecteur Windows Media devez appeler [IWMPSubscriptionService2 ::d eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| limite d’abonnement \_ \_ PREPAREFORSYNC       | 0X20  | Lecteur Windows Media devez appeler [IWMPSubscriptionService2 ::p repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| ABONNEMENTs \_ v1 \_                  | 0XF   | Par défaut. Cette valeur est utilisée si aucun n’est inscrit. Cela équivaut à la combinaison de la limite d’abonnement ALLOWPLAY, de l’abonnement Cap ALLOWCDBURN, de la limite d’abonnement \_ \_ \_ ALLOWPDATRANSFER et de la limite d' \_ \_ \_ abonnement \_ \_ BACKGROUNDPROCESSING. |



 

**Entrées de Registre pour le développement et le test**

Lorsque vous commencez à développer votre boutique en ligne, Microsoft vous propose deux clés : une clé de test et une clé de production. pendant la phase de développement et de test, votre magasin en ligne s’affiche dans Lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur. Pour plus d’informations sur les clés de test et de production, consultez [clés de test et de production pour un magasin de type 2 en ligne](test-and-production-keys-for-a-type-2-online-store.md).

Placez votre clé de test ou de production à l’emplacement suivant dans le registre.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Notez que la valeur de l’entrée de Registre TestParameter peut spécifier plusieurs clés de test ou de production. Par exemple, supposons que Proseware a une clé de test de « 1234 » et que contoso a une clé de test « 2345 ». l’entrée de registre suivante spécifie que les banques de test pour proseware et Contoso s’affichent dans Lecteur Windows Media.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Entrée de Registre ActiveService**

lorsque l’utilisateur active un magasin en ligne, Lecteur Windows Media écrit dans le registre des informations qui identifient le magasin en ligne actif. Lecteur Windows Media place les informations à l’emplacement suivant dans le registre sur l’ordinateur de l’utilisateur.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Dans la syntaxe précédente du Registre, *serviceInfo* est un espace réservé pour une chaîne qui contient des informations descriptives sur le magasin en ligne actif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





