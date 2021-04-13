---
title: " include"
description: La directive \ include force le compilateur de ressources à traiter le fichier spécifié dans le paramètre filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383767"
---
# <a name="-include"></a>inclusion

La directive **\# include** force le compilateur de ressources à traiter le fichier spécifié dans le paramètre *filename* . Ce fichier doit être un fichier d’en-tête qui définit les constantes utilisées dans le fichier de définition de ressource. Le fichier peut utiliser des caractères codés sur un octet, codés sur deux octets ou Unicode.

``` syntax
#include filename
```

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extension*
</dt> <dd>

Nom du fichier à inclure. Si le fichier se trouve dans le répertoire actif, la chaîne doit être placée entre guillemets doubles ; Si le fichier se trouve dans le répertoire spécifié par la variable d’environnement INCLUDe, la chaîne doit être placée dans des caractères inférieur à et supérieur à (<>). Vous devez fournir un chemin d’accès complet placé entre guillemets doubles (") si le fichier ne se trouve pas dans le répertoire actif ou dans le répertoire spécifié par la variable d’environnement INCLUDe.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez l’instruction suivante dans votre fichier d’en-tête pour entourer les instructions qui peuvent être compilées par un compilateur C, mais pas RC :

``` syntax
#ifndef RC_INVOKED
```

De cette façon, vous pouvez utiliser les mêmes fichiers include dans vos fichiers. c et. rc.

## <a name="example"></a>Exemple

Cet exemple traite les fichiers d’en-tête Windows. h et MyDefs. h lors de la compilation du fichier de définition de ressource :

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




