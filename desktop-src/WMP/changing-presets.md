---
title: Modification des présélections
description: Modification des présélections
ms.assetid: f8a5565d-676b-4679-a4cb-4bd7551cf41c
keywords:
- visualisations, exemple d’éclat
- visualisations personnalisées, exemple d’éclat
- Guide de programmation, visualisations
- exemples, visualisation lumineuse
- Exemple de visualisation lumineuse
- visualisations, présélections
- visualisations personnalisées, présélections
- présélections dans les visualisations, échantillon lumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d24841c95c3fc1029aa0c405e90b329799fdbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512044"
---
# <a name="changing-presets"></a>Modification des présélections

Les sections de code prédéfinies suivantes ont été modifiées pour autoriser trois présélections :

## <a name="getpresettitle"></a>GetPresetTitle

Ce code a été inséré à la place du code prédéfini généré :


```C++
    switch (nPreset)
    {
    case PRESET_RED:
        bstrTemp.LoadString(IDS_REDPRESETNAME); 
        break;

    case PRESET_GREEN:
        bstrTemp.LoadString(IDS_GREENPRESETNAME); 
        break;

    case PRESET_BLUE:
        bstrTemp.LoadString(IDS_BLUEPRESETNAME); 
        break;
    }

```



## <a name="enumerations"></a>Énumérations

L’énumération suivante dans lueur. h a été modifiée pour autoriser trois présélections :


```C++
enum {
    PRESET_RED = 0,
    PRESET_GREEN,
    PRESET_BLUE,
    PRESET_COUNT
};

```



## <a name="resource-header"></a>En-tête de ressource

Les ressources suivantes ont été définies dans Resource. h pour autoriser trois présélections :


```C++
#define IDS_REDPRESETNAME               102
#define IDS_GREENPRESETNAME             103
#define IDS_BLUEPRESETNAME              104

```



Notez que vous devez également modifier le numéro de ressource de la **\_ \_ \_ \_ valeur APS Next SYMED** sur 106.

## <a name="resource-file"></a>Fichier de ressources

Les chaînes suivantes doivent être modifiées dans le fichier Glowdll. RC pour autoriser trois présélections et leur donner des noms :


```C++
    IDS_REDPRESETNAME       "Glow Red"
    IDS_GREENPRESETNAME     "Glow Green"
    IDS_BLUEPRESETNAME      "Glow Blue"

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**L’exemple lueur**](the-glow-sample.md)
</dt> </dl>

 

 




