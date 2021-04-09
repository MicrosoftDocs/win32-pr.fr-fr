---
title: attribut helpstringdll
description: L’attribut \ helpstringdll \ définit le nom de la DLL à utiliser pour effectuer une recherche de chaîne de document.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- MIDL de l’attribut helpstringdll
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940890"
---
# <a name="helpstringdll-attribute"></a>attribut helpstringdll

L’attribut **\[ helpstringdll \]** définit le nom de la dll à utiliser pour effectuer une recherche de chaîne de document.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Help-Text-String* 
</dt> <dd>

Chaîne de caractères se terminant par zéro qui spécifie le nom de fichier complet d’une DLL.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à l’instruction Library dans son ensemble.

</dd> <dt>

*nom de la bibliothèque* 
</dt> <dd>

Identificateur que les composants logiciels utiliseront pour désigner cette [**bibliothèque**](library.md).

</dd> <dt>

*Bibliothèque-définition-instructions* 
</dt> <dd>

Une ou plusieurs instructions MIDL qui définissent l’interface de la [**bibliothèque**](library.md).

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez l’attribut **\[ helpstringdll \]** sur une instruction Library pour spécifier, sous la forme d’une chaîne de caractères, le nom de fichier complet d’une bibliothèque de liens dynamiques. Cela permet à un utilisateur d’afficher une description de la DLL avec l’Explorateur d’objets.

Utilisez les fonctions **GetDocumentation2** dans les interfaces **ITypeLib2** et **ITypeInfo2** pour récupérer la chaîne d’aide.

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

 

 