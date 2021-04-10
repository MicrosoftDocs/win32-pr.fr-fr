---
title: include (attribut)
description: L’instruction include ACF spécifie un ou plusieurs fichiers d’en-tête à inclure dans le code stub généré.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- inclure MIDL de l’attribut
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100873"
---
# <a name="include-attribute"></a>include (attribut)

L’instruction **include** ACF spécifie un ou plusieurs fichiers d’en-tête à inclure dans le code stub généré.

``` syntax
include filenames;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*noms* 
</dt> <dd>

Spécifie le nom d’un ou plusieurs fichiers d’en-tête du langage C. Utilisez le nom de fichier complet, y compris le. Extension H et mettez chaque nom de fichier entre guillemets. Séparez les noms de fichiers d’en-tête en langage C par des virgules.

</dd> </dl>

## <a name="remarks"></a>Notes

À la suite de l’instruction **include** , le code stub généré contient une instruction **\# include** de préprocesseur C. Vous fournissez le fichier d’en-tête du langage C lors de la compilation des stubs. Les instructions include s’appuient sur le mécanisme de compilateur C pour rechercher les fichiers inclus dans la structure de répertoires.

> [!Note]  
> Utilisez la directive [**Import**](import.md) plutôt que la directive **include** pour les fichiers système qui contiennent des types de données que vous souhaitez mettre à la disposition du fichier IDL. La directive **Import** ignore les prototypes de fonction et vous permet d’utiliser des commutateurs du compilateur MIDL qui optimisent la génération de routines de prise en charge.

 

## <a name="examples"></a>Exemples

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**port**](import.md)
</dt> <dt>

[Importation de fichiers et de bibliothèques de types](importing-files-and-type-libraries.md)
</dt> <dt>

[Importation de fichiers d’en-tête système](importing-system-header-files.md)
</dt> </dl>

 

 




