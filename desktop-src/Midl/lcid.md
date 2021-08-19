---
title: LCID (attribut)
description: L’attribut \ LCID \ spécifie un identificateur de paramètres régionaux et active la prise en charge du compilateur MIDL spécifique aux paramètres régionaux.
ms.assetid: 40457a1a-251c-41cd-bfa6-9d506601ff5e
keywords:
- attribut LCID MIDL
topic_type:
- apiref
api_name:
- lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87d1b6105d7e6ae561d7409cbf256b67f965c61e235ffc5782594cb5623497c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806795"
---
# <a name="lcid-attribute"></a>LCID (attribut)

L’attribut **\[ LCID \]** spécifie un identificateur de paramètres régionaux et active la prise en charge du compilateur MIDL spécifique aux paramètres régionaux.

``` syntax
[
    uuid(uuid-number), 
    lcid(localeID)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}

function-name([parameter-attribute-list, lcid] long  parameter-name,. . .);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*UUID-Number* 
</dt> <dd>

Spécifie un numéro d’identification unique universel pour la [**bibliothèque**](library.md).

</dd> <dt>

*localeID* 
</dt> <dd>

spécifie l’identificateur de paramètres régionaux 32 bits utilisé dans Windows prise en charge des langues nationales. En général, l’identificateur de paramètres régionaux est fourni au format hexadécimal.

</dd> <dt>

*Optional-attribute-List* 
</dt> <dd>

Zéro, un ou plusieurs attributs à appliquer à la [**bibliothèque**](library.md).

</dd> <dt>

*nom de la bibliothèque* 
</dt> <dd>

Nom par lequel les composants logiciels font référence à la [**bibliothèque**](library.md).

</dd> <dt>

*Bibliothèque-définition-instructions* 
</dt> <dd>

Une ou plusieurs instructions MIDL qui définissent le contenu de la [**bibliothèque**](library.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Spécifie le nom de la fonction dans le fichier IDL.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL qui seront appliqués au paramètre de fonction.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le nom du paramètre dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Remarques

La syntaxe **\[ \] LCID** a deux formes différentes ; l’effet de l’attribut dépend de la syntaxe que vous utilisez, à savoir la syntaxe de l’instruction de la [**bibliothèque**](library.md) ou la syntaxe du paramètre.

En cas d’application à l’instruction [**Library**](library.md) , avec un argument LocaleID, comme indiqué dans le premier exemple, l’attribut **\[ LCID \]** identifie les paramètres régionaux d’une bibliothèque de types ou d’un argument de fonction, et vous permet d’utiliser des caractères internationaux dans le bloc de bibliothèque.

Efficace avec la version 3.01.75 du compilateur MIDL, l’identificateur de paramètres régionaux fourni par cet attribut décore la bibliothèque de types résultante, mais modifie en fait le comportement du compilateur. Dans une instruction de [**bibliothèque**](library.md) , à partir du point où l’attribut **\[ LCID \]** est utilisé, MIDL accepte les entrées localisées en fonction des paramètres régionaux spécifiés. En particulier, la prise en charge complète des langues asiatiques telles que le japonais, le chinois et le coréen (prise en charge complète des caractères DBCS) est disponible. Les fonctionnalités prises en charge par la localisation sont les suivantes : commentaires, chaînes, HelpStrings et identificateurs.

Utilisez le commutateur [**/LCID**](-lcid.md) du compilateur pour que cette prise en charge de la localisation soit disponible pour l’ensemble du fichier d’entrée, y compris le nom de fichier et le chemin d’accès au répertoire, plutôt que simplement à l’intérieur du bloc de bibliothèque.

Lorsqu’il est appliqué à un paramètre, l’attribut **\[ LCID \]** vous permet de passer un identificateur de paramètres régionaux à une fonction, comme indiqué dans le deuxième exemple. Les restrictions suivantes s’appliquent aux paramètres **\[ LCID \]** :

-   Une fonction ne peut avoir qu’un seul paramètre **\[ LCID \]** .
-   Le type de données du paramètre doit être [**long**](long.md).
-   La direction du paramètre doit être **\[** [**dans**](in.md) **\]** uniquement.
-   Le paramètre **\[ LCID \]** doit suivre tous les autres paramètres, à l’exception d’un **\[** paramètre [**retVal**](retval.md) **\]** .
-   Vous ne pouvez pas appliquer l’attribut **\[ LCID \]** à un paramètre [**dispinterface**](dispinterface.md) ou [**coclass**](coclass.md) .

## <a name="examples"></a>Exemples

``` syntax
[  
    uuid(12345678-1234-1234-1234-123456789ABC),
    lcid(0x09),
    version(1.0)
] 
library MyLibrary
{
    /* Library definition statements */
};

interface IMyFace : IDispatch
{
    [propget] HRESULT MyFunc([in, lcid] long LocaleID,
                          [out, retval] BSTR * ReturnVal);
    // Other interface definition statements
}
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**coclasse**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**/LCID**](-lcid.md)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 