---
description: Disposition des clés de Registre
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Disposition des clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514904"
---
# <a name="layout-of-the-registry-keys"></a>Disposition des clés de Registre

Les filtres DirectShow sont enregistrés à deux emplacements :

-   La DLL qui contient le filtre est inscrite en tant que serveur COM du filtre. Quand une application appelle **CoCreateInstance** pour créer le filtre, la bibliothèque COM Microsoft Windows utilise cette entrée de Registre pour localiser la dll.
-   Des informations supplémentaires sur le filtre peuvent être inscrites dans une catégorie de filtre. Ces informations permettent à l' [énumérateur de périphérique système](system-device-enumerator.md) et au [Mappeur de filtre](filter-mapper.md) de localiser le filtre.

Les filtres ne sont pas requis pour enregistrer les informations de filtre supplémentaires. Tant que la DLL est inscrite en tant que serveur COM, une application peut créer le filtre et l’ajouter à un graphique de filtre. Toutefois, si vous souhaitez que votre filtre soit détectable par l’énumérateur du périphérique système ou le mappeur de filtre, vous devez enregistrer les informations supplémentaires.

L’entrée de Registre pour la DLL a les clés suivantes :


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



L’entrée de Registre pour les informations de filtre a les clés suivantes :


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



GUID d’une catégorie de filtre. (Voir les [catégories de filtre](filter-categories.md).) Les informations de filtre sont compressées dans un format binaire. L’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) décompresse ces données lors de la recherche d’un filtre dans le registre.

Tous les GUID de catégorie de filtre sont répertoriés dans le Registre sous la clé suivante :


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



