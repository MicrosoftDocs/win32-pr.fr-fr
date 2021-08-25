---
title: Extraction des exemples de code
description: Bien que les exemples de code soient divisés en une série de leçons du didacticiel, les exemples de regroupements appropriés peuvent être facilement extraits de la collection.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034949"
---
# <a name="extracting-the-code-samples"></a>Extraction des exemples de code

Bien que les exemples de code soient divisés en une série de leçons du didacticiel, les exemples de regroupements appropriés peuvent être facilement extraits de la collection. La plupart des exemples de répertoires individuels sont conçus pour fonctionner conjointement avec au moins un autre répertoire d’exemples. Les exemples liés aux composants se composent d’une paire client/serveur, le serveur nécessitant l’utilisation de l’utilitaire REGISTER Sample. Voici un résumé des regroupements d’exemples et comment extraire chaque groupe comme une unité qui peut être générée. Pour chaque exemple de regroupement, copiez le contenu des répertoires affichés. Le \[ \] Répertoire de destination parent indiqué ne requiert aucun contenu de la branche Samples. Toutefois, les menus d’aide des exemples en cours d’exécution partent du principe que le didacticiel approprié .HTM fichiers d’aide se trouvent dans ce \[ Répertoire de destination parent \] .

Pour l’application Win32 READTUT :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Pour l’application squelette Win32 EXE :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Pour la structure de la DLL Win32 :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Pour obtenir des exemples d’objets COM de base :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Pour les exemples de client/serveur de composant DLL in-process de base :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Pour les exemples de client/serveur de composants sous licence :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Pour les exemples de marshaling standard :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Pour obtenir des exemples de client/serveur locaux hors processus :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Pour obtenir des exemples de client/serveur cloisonnés :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Pour obtenir des exemples de client/serveur DCOM (Distributed COM) :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Pour obtenir les exemples de client/serveur gratuits :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Pour obtenir des exemples de client/serveur d’objets COM connectables :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Pour obtenir des exemples de client/serveur de stockage structuré :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Pour obtenir des exemples d’objets client/serveur persistants :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Pour obtenir des exemples de client/serveur de sécurité DCOM :

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




