---
title: attribut DllName (STR)
description: L’attribut \ DllName \ définit le nom de la DLL qui contient les points d’entrée d’un module.
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- attribut DllName (STR) MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db6f70fb65822a63bd2bf0f9919ac1b9554a664d1ac7ec9775c611b5b4e7f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067289"
---
# <a name="dllnamestr-attribute"></a>attribut DllName (STR)

L’attribut **\[ DllName \]** définit le nom de la dll qui contient les points d’entrée d’un module.

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
    [, optional-attribute-list]
]
module modulename
{
    elementlist
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour le [**module**](module.md).

</dd> <dt>

*extension* 
</dt> <dd>

Spécifie une chaîne terminée par le caractère NULL qui contient le chemin d’accès complet au fichier dll.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie une liste de zéro, un ou plusieurs attributs d’interface MIDL.

</dd> <dt>

*NomModule* 
</dt> <dd>

Spécifie le nom que d’autres composants logiciels peuvent utiliser pour faire référence au module.

</dd> <dt>

*elementlist* 
</dt> <dd>

Spécifie une ou plusieurs instructions de définition d’élément de module.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’attribut **\[ DllName \]** est requis sur un module.

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**modules**](module.md)
</dt> <dt>

[**mention**](entry.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 