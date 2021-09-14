---
title: Importation de fichiers d’en-tête système
description: S’il est souvent possible d’utiliser la directive \ include pour inclure des fichiers d’en-tête dans votre fichier IDL, ce n’est pas recommandé.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importation de MIDL, fichiers d’en-tête système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093498"
---
# <a name="importing-system-header-files"></a>Importation de fichiers d’en-tête système

S’il est souvent possible d’utiliser la directive **\# include** pour inclure des fichiers d’en-tête dans votre fichier IDL, ce n’est pas recommandé. Le compilateur MIDL génère des stubs pour toutes les fonctions définies dans le fichier IDL en cours de compilation. En général, un fichier d’en-tête contient un certain nombre de prototypes que vous n’avez pas besoin d’inclure dans vos fichiers stub, et un **\# include** place efficacement toutes ces définitions dans votre fichier IDL principal. En outre, si des types non accessibles à distance sont définis dans le fichier d’en-tête, le fichier IDL peut ne pas se compiler.

Il existe deux façons d’inclure des définitions de types à partir de fichiers d’en-tête dans un fichier IDL :

-   Utilisez la directive [**Import**](import.md) pour inclure les types de données définis dans un fichier d’en-tête. Contrairement à la directive **\# include** du langage C, la directive **Import** sélectionne uniquement les définitions de type et de constante et ignore les prototypes de procédure. Cette approche fonctionne tant que votre fichier IDL principal ne fait pas référence à des types non accessibles à distance définis dans le fichier d’en-tête.
-   Créez un fichier IDL d’assistance avec une interface factice qui comprend les fichiers d’en-tête. Ensuite, utilisez la directive [**Import**](import.md) pour inclure le fichier d’assistance. De cette façon, seuls les [**typedef**](typedef.md)s s’affichent dans les stubs compilés. Par exemple :

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
