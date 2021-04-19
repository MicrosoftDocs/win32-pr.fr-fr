---
description: Comprend le contenu d’un fichier MOF dans un autre fichier MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520736"
---
# <a name="include"></a>' #include'
/* Titre : MyMof. mof                           *//*   title : MyMof2. mof */

La \# commande inclure le préprocesseur inclut le contenu d’un fichier MOF dans un autre fichier MOF. L’exemple de code suivant décrit la syntaxe de la \# commande include.

``` syntax
#include ("Moffile.mof")
```

Dans l’exemple précédent, Moffile. MOF est le nom du fichier MOF à inclure.

L’exemple suivant montre deux fichiers MOF. Quand vous compilez le premier fichier MOF, le compilateur compile automatiquement le deuxième fichier MOF (Mymof2. MOF) à l’emplacement où vous placez l' \# instruction include.

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

Le fichier MOF suivant est inclus dans l’exemple précédent :

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 



