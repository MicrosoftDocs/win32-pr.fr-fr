---
description: API d’encodeur
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119946"
---
# <a name="encoder-api"></a>API d’encodeur

L’API d’encodeur fournit une interface uniforme pour la configuration des encodeurs logiciels et matériels. Les applications peuvent utiliser l’API d’encodeur pour configurer un encodeur et stocker les paramètres de configuration. Les fournisseurs d’encodeurs peuvent utiliser l’API d’encodeur pour exposer les fonctionnalités d’un encodeur. Bien que l’API d’encodeur soit principalement conçue pour les encodeurs, il est assez général que les décodeurs puissent également le prendre en charge.

L’API d’encodeur est exposée aux applications via l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , qui est exposée par le filtre d’encodeur. le filtre d’encodeur peut être un filtre de DirectShow natif, un encodeur matériel ou un objet de média DirectX (DMO).

-   filtres logiciels : un encodeur qui est implémenté en tant que filtre de DirectShow natif doit exposer directement le [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .
-   Encodeurs matériels : l’appareil d’encodage est exposé via un ou plusieurs AVStream minipilotes, qui sont représentés en mode utilisateur par KSProxy. KSProxy convertit les appels de méthode [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) en jeux de propriétés KS. Pour plus d’informations, consultez la documentation du DDK.
-   DMOs : le DMO doit exposer l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) . DirectShow applications peuvent interroger le filtre de Wrapper DMO, qui expose l’interface en regroupant les DMO. les Applications qui ne sont pas basées sur DirectShow peuvent interroger directement le DMO.

### <a name="encoder-capabilties"></a>Fonctionnalité encodeur

Un encodeur peut inscrire une liste de fonctionnalités de haut niveau en les stockant dans le registre système. Chaque fonctionnalité est identifiée par un GUID. Pour énumérer les fonctionnalités d’un encodeur particulier, procédez comme suit :

1.  Créez le moniker qui représente le filtre de l’encodeur. (Consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).)
2.  Interrogez le moniker de filtre de l’interface [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .
3.  Appelez [**IGetCapabilitiesKey :: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey). La méthode retourne un handle vers la clé de Registre qui contient la liste des fonctionnalités du filtre.
4.  Appelez la fonction **RegEnumValue** pour énumérer les valeurs de la clé retournée.

Si vous devloping un encodeur, créez les entrées de Registre pour les fonctionnalités lorsque le filtre est inscrit. Pour les filtres logiciels, créez une clé nommée **fonctionnalités** qui est adjacente aux clés **FilterData** et **FriendlyName** . En règle générale, vous ajoutez ces informations après avoir appelé [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) pour enregistrer les données de filtre standard. pour plus d’informations, consultez [comment inscrire des filtres de DirectShow](how-to-register-directshow-filters.md). Vous pouvez également créer une clé **CapabilitiesLocation** qui contient une chaîne indiquant l’emplacement de la clé de **fonctionnalités** dans le registre. La chaîne doit commencer par « HKLM \\ », « HKCR \\ » ou « HKCU \\ » pour indiquer la sous-arborescence du Registre. Pour les appareils Plug-and-Play, les fichiers d’installation du pilote doivent créer une clé de **fonctionnalités** adjacente à la clé **FriendlyName** du filtre, ou utiliser une clé **CapabilitiesLocation** comme décrit pour les filtres logiciels.

Une fois que vous avez créé la clé de **fonctionnalités** , créez une valeur pour chaque GUID de fonctionnalité. Le nom de la valeur doit être la forme de chaîne du GUID, sous la forme `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . Chaque type de valeur doit être l’un des suivants :

-   Valeur numérique unique. Utilisez une valeur **DWORD** .
-   GUID (identificateur global unique). Utilisez la forme de chaîne du GUID.
-   Paires numériques. Utilisez une chaîne sous la forme « a, b » pour représenter des paires de valeurs, telles que la largeur et la hauteur, ou le numérateur et le dénominateur pour les fractions.
-   Tableaux de valeurs. Utilisez des chaînes multiples (**reg \_ SZ \_ multi**) pour représenter plusieurs valeurs.

L’exemple suivant illustre la disposition du Registre pour un filtre logiciel :


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a>Profils d’encodeur

Un *profil d’encodeur* est une liste fixe de paramètres de configuration qui peuvent être appliqués à un encodeur au moment de l’exécution. Les profils sont indépendants de l’encodeur ; une application peut sélectionner un encodeur, puis sélectionner un profil et appliquer les paramètres de profil à l’encodeur. Les profils sont identifiés par un GUID et doivent être stockés à l’emplacement suivant dans le registre :


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



*GUID du profil* de l’emplacement

forme de chaîne du GUID qui identifie le profil. Créez des valeurs pour chaque paramètre. Créez également une valeur de chaîne nommée « FriendlyName » dont les données identifient le profil (par exemple, « LowBandwidthVideo »).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’encodeur et de décodeur](encoder-and-decoder-development.md)
</dt> </dl>

 

 



