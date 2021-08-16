---
title: helpfile (attribut)
description: L’attribut \ HelpFile \ définit le nom du fichier d’aide d’une bibliothèque de types. Tous les types d’une bibliothèque partagent le même fichier d’aide.
ms.assetid: caa248b1-a1a7-4c36-886a-079a66a01907
keywords:
- attribut HelpFile MIDL
topic_type:
- apiref
api_name:
- helpfile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1557d96f35913e5e1ed9b784bedfc430e6c4d77b65954583ca6923e4728af9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384019"
---
# <a name="helpfile-attribute"></a>helpfile (attribut)

L’attribut **\[ HelpFile \]** définit le nom du fichier d’aide d’une bibliothèque de types. Tous les types d’une bibliothèque partagent le même fichier d’aide.

``` syntax
[
    uuid(uuid-number), 
    helpfile("filename") 
    [, optional-attribute-list]
] 
library 
{
    library statements
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md).

</dd> <dt>

*extension* 
</dt> <dd>

Spécifie le nom du fichier contenant le texte d’aide.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs que le compilateur MIDL appliquera à la [**bibliothèque**](library.md).

</dd> <dt>

*instructions de bibliothèque* 
</dt> <dd>

Spécifie une ou plusieurs instructions MIDL qui définissent l’interface de la bibliothèque.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez les fonctions **GetDocumentation** dans les interfaces **ITypeLib** et **ITypeInfo** pour récupérer le nom de fichier.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpfile("filename.hlp"),
    lcid(0x0409), 
    version(2.0)
]
library Hello
{
    /* Library definition statements here. */
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 