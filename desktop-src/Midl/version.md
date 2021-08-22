---
title: version (attribut)
description: L’attribut \ version \ de l’interface identifie une version particulière parmi plusieurs versions d’une interface RPC. Avec l’attribut version, vous vous assurez que seules les versions compatibles du logiciel client et serveur sont autorisées à se lier.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- MIDL, attribut de version
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c72cc825183740d856c20b9e5c76ece472f82db405d9560e6502f6e32985b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252109"
---
# <a name="version-attribute"></a>version (attribut)

L’attribut d’interface de **\[ version \]** identifie une version particulière parmi plusieurs versions d’une interface RPC. Avec l’attribut version, vous vous assurez que seules les versions compatibles du logiciel client et serveur sont autorisées à se lier.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur Major* 
</dt> <dd>

Spécifie un entier non signé Short compris entre zéro et 65 535 inclus, qui représente le numéro de version principale.

</dd> <dt>

*valeur mineure* 
</dt> <dd>

Spécifie un entier non signé Short compris entre zéro et 65 535 inclus, qui représente le numéro de version secondaire. La valeur de la version mineure est facultative. Si elle est présente, la valeur de la version mineure est séparée du numéro de version principale par un point (.). S’il n’est pas spécifié, la valeur de la version mineure est égale à zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le compilateur MIDL ne prend pas en charge plusieurs versions d’une interface COM. Par conséquent, une liste d’attributs d’interface qui inclut l’attribut d' **\[** [**objet**](object.md) **\]** ne peut pas inclure l’attribut de **\[ version \]** . Pour créer une nouvelle version d’une interface COM existante, utilisez l’héritage de l’interface. Une interface COM dérivée possède un UUID différent, mais hérite des fonctions membres d’interface, des codes d’État et des attributs d’interface de l’interface de base.

En association avec la **\[** [](uuid.md) **\]** valeur UUID, la valeur de **\[ version \]** identifie de manière unique l’interface. La bibliothèque Runtime transmet la **\[ version \]** et les valeurs **\[ UUID \]** au serveur lorsque le client appelle une fonction distante. Un client peut effectuer une liaison à un serveur pour une interface donnée dans les cas suivants :

-   La valeur **\[ UUID \]** est la même.
-   Le numéro de version principale est le même.
-   Le numéro de version mineure du client est inférieur ou égal au numéro de version secondaire du serveur.

C’est à votre avantage et à l’avantage de permettre à vos utilisateurs de conserver une compatibilité ascendante entre les versionsÂ, c’est-à-dire de modifier l’interface afin que seul le numéro de version mineure soit modifié. Vous pouvez conserver une compatibilité ascendante lorsque vous ajoutez de nouveaux types de données qui ne sont pas utilisés par les fonctions existantes et lorsque vous ajoutez de nouvelles fonctions sans modifier la spécification d’interface pour les fonctions existantes.

Modifiez le numéro de version principale si l’une des conditions suivantes s’applique :

-   Si vous modifiez un type de données utilisé par une fonction existante.
-   Si vous modifiez la spécification d’interface d’une fonction existante (telle que l’ajout ou la suppression d’un paramètre).
-   Si vous ajoutez des rappels qui sont appelés par des fonctions existantes.

Modifiez le numéro de version mineure si toutes les conditions suivantes s’appliquent :

-   Si vous ajoutez des définitions ou des constantes de type qui ne sont pas utilisées par des fonctions ou des rappels existants.
-   Si vous ne modifiez pas les fonctions existantes et que vous ajoutez de nouvelles fonctions à l’interface.
-   Si vous ajoutez des rappels qui ne sont pas appelés par des fonctions existantes et que les nouveaux rappels suivent les fonctions existantes.

Si vos modifications qualifient comme une modification à compatibilité descendante de l’interface, utilisez la procédure suivante.

**Pour modifier le fichier d’interface (IDL)**

1.  Ajoutez de nouvelles définitions de constantes et de types au fichier d’interface.
2.  Ajoutez des fonctions de rappel à la fin du fichier d’interface.
3.  Ajoutez de nouvelles fonctions à la fin du fichier d’interface.

L’attribut **\[ version \]** peut se produire au plus une fois dans l’en-tête de l’interface.

Lorsque l’attribut version n’est pas présent, l’interface a une version par défaut de 0,0.

Le point entre les nombres principaux et secondaires est un délimiteur et ne représente pas une virgule décimale. Le nombre mineur est traité comme un entier. Les zéros non significatifs ne sont pas significatifs. Les zéros de fin sont significatifs.

Par exemple, le paramètre de version 1,11 représente une valeur majeure d’un et une valeur mineure de onze. La version 1,11 ne représente pas une valeur comprise entre 1,1 et 1,2.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**dessin**](object.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> </dl>

 

 




