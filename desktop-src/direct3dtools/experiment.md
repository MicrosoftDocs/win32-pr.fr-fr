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
ms.openlocfilehash: 90e60f3f197db78a3ec399c2f8ffe7144901b097
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625365"
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

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



