---
title: Présélections
description: Présélections
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- visualisations, présélections
- visualisations personnalisées, présélections
- visualisations, présélection de la barre
- visualisations personnalisées, présélection de barre
- visualisations, présélection d’onde
- visualisations personnalisées, présélections Wave
- visualisations, fonction Render
- visualisations personnalisées, fonction Render
- Fonction Render, présélections
- visualisations, fonction GetPresetTitle
- visualisations personnalisées, fonction GetPresetTitle
- GetPresetTitle fonction)
- énumérations, présélections de visualisation
- visualisations, énumérations
- visualisations personnalisées, énumérations
- visualisations, en-tête de ressource et chaînes
- visualisations personnalisées, en-tête de ressource et chaînes
- présélections dans les visualisations, présélection de la barre
- présélections dans les visualisations, présélection d’onde
- présélections dans les visualisations, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196626"
---
# <a name="presets"></a>Présélections

Les présélections sont fournies comme un moyen d’avoir différents effets provenant de la même visualisation. Par exemple, vous pouvez créer un effet d’éclat généré par un bloc de code, mais utiliser une présélection pour déterminer la couleur de la lueur. Les noms de présélections peuvent être rouge, vert et bleu.

L’Assistant définit deux présélections pour le code qu’il génère. L’un est appelé bar et l’autre est appelé Wave. La présélection barres affiche des barres qui affichent l’activité dans le spectre audio et utilisent les données de forme d’onde. La présélection de l’onde affiche une ligne de tremblement qui indique la puissance audio de la forme d’onde.

Si vous modifiez l’une des informations prédéfinies, vous devez également modifier les éléments suivants du code généré.

## <a name="render-function"></a>Render, fonction

La fonction **IWMPEffects :: Render** se trouve dans le fichier *nom_projet*. cpp, où *ProjectName* est le nom du projet que vous avez choisi lors de l’exécution de l’Assistant.

Le code généré dans la fonction **Render** utilise une instruction switch pour choisir entre deux présélections. La présélection actuelle est celle que l’utilisateur sélectionne dans le lecteur Windows Media. Si vous souhaitez modifier le code qui s’exécute pour une présélection particulière ou ajouter ou soustraire une présélection, modifiez l’instruction switch en conséquence.

Les deux présélections sont définies par **les \_ barres prédéfinies** et les énumérations de **\_ portée prédéfinies** . Le choix de la présélection qui sera appelée est défini par m \_ nPreset.

## <a name="getpresettitle"></a>GetPresetTitle

La fonction **IWMPEffects :: GetPresetTitle** se trouve dans le fichier *nom_projet*. cpp, où *ProjectName* est le nom du projet que vous avez choisi lors de l’exécution de l’Assistant.

La fonction **GetPresetTitle** définit les relations entre les énumérations prédéfinies et les ressources de type chaîne. Les **\_ barres prédéfinies** des énumérations et les **\_ étendues prédéfinies** sont générées par l’Assistant et utilisent les ID de ressources de chaîne \_ BARSPRESETNAME et IDS \_ SCOPEPRESETNAME.

Vous devez modifier les énumérations et les ressources de type chaîne si vous ajoutez, soustrayez ou modifiez des présélections.

## <a name="preset-enumerations"></a>Énumérations prédéfinies

L’énumération prédéfinie est définie dans le fichier *nom_projet*. h, où *ProjectName* est le nom du projet que vous avez choisi lors de l’exécution de l’Assistant.

L’énumération définit les deux présélections actuelles et le nombre. Si vous ajoutez ou soustrayez des présélections ou modifiez l’énumération, veillez à modifier cette énumération afin que le nombre et l’ordre des présélections soient corrects. Cette énumération est utilisée pour s’assurer que vous appelez la présélection appropriée dans la fonction **Render** .

## <a name="resource-header"></a>En-tête de ressource

Vous devez définir les ressources pour les noms de votre présélection dans le fichier d’en-tête Resource. h. Les présélections actuelles sont définies comme suit :


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Si vous ajoutez ou soustrayez des présélections, vous devez modifier l’en-tête de ressource et les nombres correspondant.

## <a name="resource-strings"></a>Chaînes de ressources

Les noms réels des présélections sont définis dans le fichier de ressources *ProjectName* dll. RC, où *nom_projet* est le nom du projet que vous avez choisi lors de l’exécution de l’Assistant. Vous pouvez modifier ce fichier manuellement ou utiliser l’éditeur de ressources inclus avec Microsoft Visual C++.

Les noms générés sont le nom de la visualisation plus la présélection spécifique. Le fichier de ressources du code généré les définit comme suit :


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



où *nom_projet* est le nom du projet que vous avez choisi lors de l’exécution de l’Assistant. C’est à cet endroit que vous allez modifier les noms réels des présélections, et c’est ainsi que le lecteur Windows Media les appelle et les affiche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de votre code**](implementing-your-code.md)
</dt> </dl>

 

 




