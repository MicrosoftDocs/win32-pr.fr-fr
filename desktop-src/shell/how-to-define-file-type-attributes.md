---
description: Définition des attributs de type de fichier dans le registre.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Comment définir des attributs de type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223573"
---
# <a name="how-to-define-file-type-attributes"></a>Comment définir des attributs de type de fichier

L’attribution d’attributs de type de fichier à un ProgID associé vous permet de contrôler certains aspects du comportement du type de fichier. avant Windows Vista, ces attributs pouvaient vous permettre de limiter la mesure dans laquelle l’utilisateur peut utiliser l’onglet de propriétés des **Options des dossiers** pour modifier différents aspects du type de fichier, tels que son icône ou ses verbes.

Les attributs de type de fichier sont des indicateurs binaires spécifiés en tant que valeurs **reg \_ DWORD** ou **reg \_ Binary** dans la sous-clé ProgID associée au type de fichier.

Pour affecter des attributs pour un type de fichier, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Ajoutez une entrée indicateurs à la sous-clé ProgID associée au type de fichier.

### <a name="step-2"></a>Étape 2 :

Affectez à l’entrée la valeur d’attribut appropriée.

L’exemple suivant montre les \_ attributs Association NoRemove (0x00000010) et Association \_ NoNewVerb (0x00000020) définis pour le type de fichier. MYP.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Remarques

Les indicateurs peuvent être combinés avec un ou logique pour former la valeur d’attribut unique.

Pour obtenir la liste des attributs de type de fichier possibles et leurs valeurs hexadécimales, ainsi que des détails sur la récupération et la définition par programmation de ces valeurs, consultez [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



