---
title: Inscription des plug-ins DSP
description: Inscription des plug-ins DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- plug-ins Lecteur Windows Media, entrées de registre
- plug-ins, entrées de Registre
- plug-ins de traitement de signal numérique, entrées de Registre
- Plug-ins DSP, entrées de Registre
- Registre, plug-ins DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416210"
---
# <a name="registering-dsp-plug-ins"></a>Inscription des plug-ins DSP

pour rendre le plug-in DSP disponible dans Lecteur Windows Media vous devez créer les sous-clés et les entrées de registre suivantes sur l’ordinateur de l’utilisateur.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP. Le tableau suivant décrit ces espaces réservés.



| Espace réservé               | Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID qui est l’identificateur de classe de la classe principale du plug-in DSP. Il s’agit de la classe qui implémente **IMediaObject**, **IPluginEnable** et éventuellement **ISpecifyPropertyPages**. Dans un plug-in en mode double, cette classe implémente également **IMFTransform** et **IMFGetService**. Ce GUID doit être au format de Registre, avec les accolades.<br/> Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Nom convivial de la classe principale du plug-in DSP. Exemple : « ProsewareDSP Class »<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Chemin d’accès qualifié complet à la DLL qui implémente le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDsp.dll »<br/>                                                                                                                                                                                                                                                                                     |
| *Threads*               | Chaîne qui spécifie le modèle de thread pour le plug-in. si le plug-in va s’exécuter avec Lecteur Windows Media 11 sur Windows Vista, cette entrée de registre doit être égale à « Both ». si le plug-in s’exécute sur Windows XP ou des systèmes d’exploitation plus anciens, cette entrée de registre peut être égale à « Apartment » ou « Both ».                                                                                           |



 

si votre plug-in DSP implémente une interface personnalisée et si votre plug-in va s’exécuter dans Lecteur Windows Media 11 sur Windows Vista, vous devez créer les sous-clés et les entrées de registre suivantes sur l’ordinateur de l’utilisateur.


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms, les valeurs numériques et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP. Le tableau suivant décrit ces espaces réservés.



| Espace réservé           | Description                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID qui est l’identificateur de classe de la classe qui implémente les proxies et les stubs pour les interfaces personnalisées du plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.<br/> Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | Le chemin d’accès complet à la DLL qui implémente les interfaces de proxy et stub pour le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDspPS.dll »<br/>                                                                                               |
| *CustomInterfaceId*   | GUID qui est l’identificateur d’interface d’une interface personnalisée qui est implémentée par le plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.<br/> Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | Nom d’une interface personnalisée qui est implémentée par le plug-in DSP. Exemple : « IProsewareDsp »<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | Nombre de méthodes, y compris les méthodes héritées, définies par une interface personnalisée. Exemple : « 5 »<br/>                                                                                                                                                                  |



 

Si votre plug-in DSP fournit une page de propriétés, vous devez créer les sous-clés et les entrées de Registre suivantes sur l’ordinateur de l’utilisateur.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



Dans la syntaxe précédente du Registre, les symboles en italique sont des espaces réservés pour les noms et les identificateurs globaux uniques (GUID) qui sont spécifiques au plug-in DSP. Le tableau suivant décrit ces espaces réservés.



| Espace réservé                 | Description                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID qui est l’identificateur de classe pour la classe de page de propriétés fournie par le plug-in DSP. Ce GUID doit être au format de Registre, avec les accolades.<br/> Format : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Nom convivial de la classe de la page de propriétés. Exemple : « ProsewareDSP Property page Class »<br/>                                                                                                                                     |
| *PluginModuleName*          | Chemin d’accès qualifié complet à la DLL qui implémente le plug-in DSP. Exemple : « C : \\ Program Files \\ proseware \\ProsewareDsp.dll »<br/>                                                                                               |



 

**Appel de IWMPPluginRegistrar**

Outre les sous-clés et les entrées de Registre décrites dans les listes et les tables précédentes, vous devez créer des clés et des entrées de registre en appelant [IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). cette méthode effectue l’inscription nécessaire pour permettre à Lecteur Windows Media de reconnaître votre plug-in et de le présenter en tant qu’option à l’utilisateur.

Appelez **IWMPMediaPluginRegistrar :: WMPRegisterPlayerPlugin** dans la fonction **DllRegisterServer** de votre plug-in, puis appelez [IWMPMediaPluginRegistrar :: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) dans la fonction **DllUnregisterServer** de votre plug-in. Pour obtenir un pointeur vers une interface **IWMPMediaPluginRegistrar** , appelez **CoCreateInstance**, en passant \_ le CLSID WMPMediaPluginRegistrar en tant qu’ID de classe. Le CLSID \_ de constante WMPMediaPluginRegistrar est défini dans wmpservices. h.

**Inscription dans l’Assistant de plug-in DSP**

l’assistant de plug-in DSP, qui est inclus dans le SDK Windows, génère un exemple de code basé sur Active Template Library (ATL). la fonction **DllRegisterServer** du plug-in de l’exemple appelle la fonction **RegisterServer** de ATL, qui crée des sous-clés et des entrées de registre en fonction de deux fichiers de script du registre dans le projet Visual Studio. Le fichier *ProjectName*. RGS contient le script d’enregistrement de la classe principale du plug-in, et le fichier *nom_projet* PropPage. RGS contient le script d’enregistrement de la classe de la page de propriétés du plug-in. L’exemple de fonction **DllRegisterServer** du plug-in appelle également **IWMPPluginRegistrar :: WMPRegisterPlayerPlugin**.

L’Assistant de plug-in DSP génère également du code pour un composant proxy-stub qui est un fichier de .dll auto-inscrit. Le code d’inscription de ce fichier se trouve dans dlldata. cpp. La macro **DLLDATA \_ routines** se développe pour inclure une implémentation de **DllRegisterServer**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





