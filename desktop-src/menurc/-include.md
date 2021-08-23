---
title: " include"
description: La directive \ include force le compilateur de ressources à traiter le fichier spécifié dans le paramètre filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bf5d6fa40e45073ca7ccb5f97dd3ddb0d13dfdfced965d5c83332183da421e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599718"
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

## <a name="remarks"></a>Remarques

Utilisez l’instruction suivante dans votre fichier d’en-tête pour entourer les instructions qui peuvent être compilées par un compilateur C, mais pas RC :

``` syntax
#ifndef RC_INVOKED
```

De cette façon, vous pouvez utiliser les mêmes fichiers include dans vos fichiers. c et. rc.

## <a name="example"></a>Exemples

cet exemple traite les fichiers d’en-tête Windows. h et MyDefs. h lors de la compilation du fichier de définition de ressource :

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




