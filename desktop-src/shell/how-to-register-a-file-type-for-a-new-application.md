---
description: Si vous envisagez d’associer un ou plusieurs types de fichiers à une nouvelle application, vous devez définir un ProgID pour chaque type de fichier que vous souhaitez associer à l’application.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Comment inscrire un type de fichier pour une nouvelle application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de165d378d27c6891b681f95da7242b026844bd7734709ebd272c06edf40e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859659"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Comment inscrire un type de fichier pour une nouvelle application

Si vous envisagez d’associer un ou plusieurs types de fichiers à une nouvelle application, vous devez définir un ProgID pour chaque type de fichier que vous souhaitez associer à l’application.

Pour créer un ProgID pour chaque type de fichier unique géré par votre application, procédez comme suit.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Notez que certains types de fichiers ont plusieurs extensions qui pointent vers le même ProgID ; par exemple :

-   **HKEY \_ CLASSES \_ racine** \\ **app. jpeg** (votre ProgID)
-   **HKEY \_ CLASSES \_ racine** \\ **.jpg** = App. jpeg (mappages de types de fichiers)
-   **HKEY \_ CLASSES \_ racine** \\ **. jpeg** = App. jpeg

### <a name="step-2"></a>Étape 2 :

Supprimez les valeurs ProgID lors de l’installation et de la désinstallation de votre programme.

### <a name="step-3"></a>Étape 3 :

Laissez les mappages de type de fichier inchangés au moment de la désinstallation. Cela fonctionne, car les mappages de types de fichiers sont stockés par utilisateur dans les \_ classes HKEY \_ root \\ . ext, et le système identifie le cas où la valeur ProgID est manquante et l’ignore. Le fait de laisser les mappages de types de fichiers inchangés évite d’avoir à utiliser du code conditionnel qui supprime uniquement le mappage de type de fichier si la valeur pointe encore sur votre ProgID. Il est important de ne pas le faire dans les cas où il peut avoir été modifié par une autre application et vous ne pouvez donc pas supprimer la valeur facilement.

### <a name="step-4"></a>Étape 4 :

Spécifiez une valeur unique pour la description du type de fichier de chaque ProgID de type de fichier en procédant de l’une des façons suivantes :

-   Laissez la valeur par défaut du ProgID vide, auquel cas le système utilise le fichier. ext.
-   Fournissez une valeur localisée via FriendlyTypeName et, pour la compatibilité avec les anciennes applications qui lisent directement le registre, veillez à fournir la valeur par défaut du ProgID en tant que Description du type de fichier (autrement dit, utilisez la même valeur que celle référencée par FriendlyTypeName dans la ressource anglaise).

## <a name="remarks"></a>Remarques

Si vous envisagez d’associer le fichier à une application existante, localisez un ProgID d’application dans le registre. Pour plus d’informations, consultez [types de fichiers](fa-file-types.md).

 

 



