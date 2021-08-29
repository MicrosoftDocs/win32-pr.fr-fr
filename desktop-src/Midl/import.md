---
title: import (attribut)
description: La directive import spécifie un autre fichier IDL, ODL ou d’en-tête contenant les définitions que vous souhaitez référencer à partir de votre fichier IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- MIDL d’attribut d’importation
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd389d56dff242132c628beedaf9c70d697f1fead0286aa0b59cd492a5a1e882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040070"
---
# <a name="import-attribute"></a>import (attribut)

La directive **Import** spécifie un autre fichier IDL, ODL ou d’en-tête contenant les définitions que vous souhaitez référencer à partir de votre fichier IDL principal.

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*extension* 
</dt> <dd>

Spécifie le nom du fichier d’en-tête, IDL ou ODL à importer.

</dd> </dl>

## <a name="remarks"></a>Remarques

Avec la directive **Import** , toutes les instructions IDL dans le fichier importé, telles que typedefs, déclarations de constantes et définitions d’interface, deviennent disponibles pour l’importation. Fichier IDL.

Le fichier importé est traité séparément (ce qui signifie que le préprocesseur CPP est appelé indépendamment) à partir du fichier IDL d’importation. De cette façon, les directives de préprocesseur, telles que \# define, ne reportent pas d’un fichier d’en-tête ou d’un fichier IDL importé vers le fichier IDL d’importation.

À l’instar de la macro de préprocesseur du langage C **\# include**, la directive **Import** indique au compilateur d’inclure les types de données définis dans les fichiers IDL importés. Contrairement à la directive **\# include** , la directive **Import** ignore les prototypes de procédure, car aucun stub n’est généré pour quoi que ce soit dans le fichier importé.

Pour obtenir des informations spécifiques sur l’utilisation de l' **importation** pour inclure des fichiers d’en-tête dans un fichier IDL, consultez [importation de fichiers d’en-tête système](importing-system-header-files.md).

En-tête du langage C (. H) généré pour l’interface ne contient pas directement les types importés, mais génère à la place une directive **\# include** pour le fichier d’en-tête correspondant à l’interface importée. Par exemple, lorsque vous importez la BASE. IDL dans votre dérivé. IDL, le fichier d’en-tête généré est dérivé. H contiendra la directive **\# include** base. H.

Les règles suivantes s’appliquent :

-   Le mot clé **Import** est facultatif et peut apparaître zéro, une ou plusieurs fois dans le fichier IDL.
-   Chaque mot clé **Import** peut être associé à plusieurs noms de fichier.
-   Séparez les noms de fichiers par des virgules.
-   Vous devez placer le nom de fichier entre guillemets et mettre fin à l’instruction d’importation avec un point-virgule (;).
-   Vous pouvez importer une interface qui n’a pas d’attributs dans un autre fichier IDL. Toutefois, l’interface doit contenir uniquement des types de données ; elle ne peut pas contenir de procédures. Si même une procédure est contenue dans l’interface importée, vous devez spécifier un attribut [**local**](local.md) ou [**UUID**](uuid.md) .
-   La fonction d' **importation** est idempotentÂ â €, c’est-à-dire que l’importation d’une interface plus d’une fois n’a aucun effet supplémentaire.

> [!Note]  
> Le comportement de la directive **Import** est indépendant du mode compilateur MIDL commutateurs [**/ms. \_ ext**](-ms-ext.md) (valeur par défaut), [**/OSF**](-osf.md)et [**/app \_**](-app-config.md). Toutefois, le mode de compilateur (**/OSF** ou **/ms. \_ ext**) peut affecter la décoration d’attribut de pointeur sur les types importés. Pour plus d’informations [, consultez héritage de type d’attribut de pointeur](/windows/desktop/Rpc/pointer-attribute-type-inheritance).

 

## <a name="examples"></a>Exemples

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**configuration de/App \_**](-app-config.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**inclusion**](include.md)
</dt> <dt>

[Importation de fichiers d’en-tête système](importing-system-header-files.md)
</dt> <dt>

[Importation de fichiers et de bibliothèques de types](importing-files-and-type-libraries.md)
</dt> <dt>

[**/ms. \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 