---
description: Représente des informations sur une expérience (capture).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Structure d’expérimentation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ebe9ab0232104886078256effdfaf5534144dc30421dab2ac2359ef390c0a69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118149"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span id="vspixengine.experiment"></span>Structure d’expérimentation

Représente des informations sur une expérience (capture).

## <a name="syntax"></a>Syntaxe


```C++
} Experiment;
```

## <a name="members"></a>Membres

**processId**  
ID de processus associé.

**applicationName**  
Chaîne COM contenant le nom de l’application sur laquelle exécuter l’expérience.

**commandLineArguments**  
Chaîne COM contenant les arguments de ligne de commande.

**workingDirectory**  
Chaîne COM contenant le chemin d’accès du répertoire de travail.

**tempPixRunFile**  
Chaîne COM contenant le chemin d’accès du fichier temporaire utilisé pour effectuer l’expérimentation.

**startOption**  
Option Start associée à l’expérience.

**experimentType**  
Type d’expérience (capture).

**uiLocale**  
ID des paramètres régionaux utilisés pour les éléments de superposition de l’interface utilisateur pendant le experiement (capture). cette valeur est transmise à partir de l’hôte (par exemple, Visual Studio Graphics Diagnostics) au moteur de capture.

**registryRoot**  
Chaîne COM contenant la racine du Registre. cette valeur est transmise à partir de l’hôte (par exemple, Visual Studio Graphics Diagnostics) au moteur de capture.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



