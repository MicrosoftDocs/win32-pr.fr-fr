---
title: attribut de bibliothèque
description: L’instruction Library contient toutes les informations que le compilateur MIDL utilise pour générer une bibliothèque de types.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- attribut de bibliothèque MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086369"
---
# <a name="library-attribute"></a>attribut de bibliothèque

L’instruction **Library** contient toutes les informations que le compilateur MIDL utilise pour générer une bibliothèque de types.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la bibliothèque.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie des attributs supplémentaires qui s’appliquent à l’intégralité de l’instruction **Library** . Les attributs autorisés sont les suivants : **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**helpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** et **\[** [**version**](version.md) **\]** .

</dd> <dt>

*nom de la bibliothèque* 
</dt> <dd>

Nom par lequel les composants logiciels font référence à la **bibliothèque**.

</dd> <dt>

*Bibliothèque-définition-instructions* 
</dt> <dd>

Une ou plusieurs instructions MIDL qui définissent le contenu de la **bibliothèque**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les instructions à l’intérieur du bloc de bibliothèque peuvent utiliser des éléments déclarés à l’intérieur ou à l’extérieur du bloc de bibliothèque. Les instructions de bibliothèque peuvent utiliser ces éléments comme types de base, héritant de ces éléments ou simplement en les référençant sur une ligne, comme suit :

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

Le compilateur MIDL crée une bibliothèque de types qui comprend des définitions pour chaque élément à l’intérieur du bloc de bibliothèque, ainsi que des définitions pour tous les éléments définis en dehors de et référencés à partir du bloc de bibliothèque.

Pour plus d’informations sur la génération d’une bibliothèque de types et de proxy stubs et d’en-têtes à partir d’un seul fichier IDL, consultez [génération d’une dll de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Exemples

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contenu d’une bibliothèque de types](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**régulation**](control.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**masquer**](hidden.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**sensible**](restricted.md)
</dt> <dt>

[**Version**](version.md)
</dt> </dl>

 

 