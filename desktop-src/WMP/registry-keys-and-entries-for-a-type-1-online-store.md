---
title: Clés et entrées de Registre pour un magasin de type 1 en ligne
description: Clés et entrées de Registre pour un magasin de type 1 en ligne
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Lecteur Windows Media magasins en ligne, registre
- magasins en ligne, registre
- types 1 magasins en ligne, registre
- Registre, type 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e42b1b75b64a8736c1491ccc058fe5548d78808ba51e142b3272d17d3c0eba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861529"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Clés et entrées de Registre pour un magasin de type 1 en ligne

pour rendre un magasin en ligne de type 1 disponible dans Lecteur Windows Media, le fournisseur de magasin en ligne doit créer les sous-clés et les entrées de registre suivantes sur l’ordinateur de l’utilisateur.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> La définition de la valeur de DllSurrogate sur la chaîne vide indique que le runtime COM chargera le plug-in du magasin en ligne dans le substitut de la DLL par défaut, dllhost.exe.

 

Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au magasin en ligne. Le tableau suivant décrit ces espaces réservés.



| Espace réservé    | Description                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Chaîne convenue entre Microsoft et le magasin en ligne. Cette chaîne identifie de façon unique le magasin en ligne. Exemple : « Proseware »<br/>                                                                                                                                                                                   |
| *flags*        | un or **au niveau du** bit d’une ou de plusieurs fonctionnalités de plug-in signalent que ces indicateurs spécifient si Lecteur Windows Media doit appeler des méthodes particulières de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner). Pour plus d’informations sur les indicateurs pris en charge, consultez le tableau des indicateurs de capacité de plug-in qui suit ce tableau. Exemple : 00000058<br/> |
| *identificateur*        | GUID qui est l’identificateur de classe (CLSID) de la classe qui implémente **IWMPContentPartner** dans le plug-in du magasin en ligne. Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *convivial* | Nom convivial du magasin en ligne. exemple : « proseware Musique Service »<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID qui est l’identificateur d’application (AppID) pour le plug-in du magasin en ligne. Ce GUID doit être au format de Registre, avec les accolades. Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Nom du plug-in du magasin en ligne. Exemple : « plug-in de partenaire de contenu Proseware »<br/>                                                                                                                                                                                                                                   |
| *ClassName*    | Nom de la classe qui implémente **IWMPContentpartner** dans le plug-in du magasin en ligne. Exemple : « CProsewarePartner »<br/>                                                                                                                                                                                              |
| *NomModule*   | Chemin d’accès complet à la DLL qui implémente le plug-in du magasin en ligne. Exemple : « C : \\ Program Files \\ proseware \\ProsewarePartner.dll »<br/>                                                                                                                                                                         |
| *Threading*    | Type de cloisonnement dans lequel le plug-in est exécuté. « ThreadingModel » = « Apartment » indique que le plug-in s’exécute dans un thread cloisonné (STA). "ThreadingModel" = "Free" indique que le plug-in s’exécute dans le cloisonnement multithread (MTA).                                                                                     |



 

Le tableau suivant décrit les indicateurs de capacité de plug-in.



| Indicateur                                    | Valeur | Description                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| limite d’abonnement \_ \_ BACKGROUNDPROCESSING | 0x8   | Lecteur Windows Media devez appeler [IWMPContentPartner :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) pour informer le plug-in lorsqu’il doit démarrer et arrêter le traitement en arrière-plan.                                                                                                     |
| limite d’abonnement \_ \_ DEVICEAVAILABLE      | 0x10  | Lecteur Windows Media doit appeler [IWMPContentPartner :: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| la limite d’abonnement \_ \_ est \_ CONTENTPARTNER   | 0x40  | informe Lecteur Windows Media que le plug-in implémente l’interface **IWMPContentPartner** . Tous les plug-ins de magasin en ligne de type 1 doivent définir cet indicateur.                                                                                                                         |
| limite d’abonnement \_ \_ ALTLOGIN             | 0x80  | informe Lecteur Windows Media que le plug-in prend en charge une autre connexion. si le plug-in prend en charge une autre connexion, Lecteur Windows Media récupère l’URL de connexion alternative et la légende en appelant [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Entrées de Registre pour le développement et le test**

Lorsque vous commencez à développer votre boutique en ligne, Microsoft vous propose deux clés : une clé de test et une clé de production. pendant la phase de développement et de test, votre magasin en ligne s’affiche dans Lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur. Pour plus d’informations sur les clés de test et de production, consultez [clés de test et de production pour un magasin de type 1 en ligne](test-and-production-keys-for-a-type-1-online-store.md).

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

[**Référence pour les magasins en ligne de type 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





