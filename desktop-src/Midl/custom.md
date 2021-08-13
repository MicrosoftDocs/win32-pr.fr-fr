---
title: attribut personnalisé
description: L’attribut \ custom \ crée un attribut défini par l’utilisateur.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL d’attribut personnalisé
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace6a558da428da07a432653391e0e48b7a5545bb1a83eb40d9c950abfa9d9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643668"
---
# <a name="custom-attribute"></a>attribut personnalisé

L’attribut **\[ personnalisé \]** crée un attribut défini par l’utilisateur.

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID d’attribut* 
</dt> <dd>

GUID de l’attribut personnalisé.

</dd> <dt>

*attribut-valeur* 
</dt> <dd>

Valeur que l’attribut contient. La valeur doit être une valeur qui peut être placée dans un type VARIANT.

</dd> <dt>

*liste d’attributs* 
</dt> <dd>

Autres attributs, tels que **\[** [**UUID**](uuid.md) **\]** et **\[** [**helpString**](helpstring.md) **\]** , qui s’appliquent à cet élément.

</dd> <dt>

*type d’élément* 
</dt> <dd>

Type d’élément auquel s’applique l’attribut personnalisé. Il peut s’agir d’une instruction de bibliothèque, d’informations de type, d’une variable, d’une fonction ou d’un paramètre. Vous ne pouvez pas utiliser un attribut personnalisé sur un membre d’une coclasse.

</dd> <dt>

*nom de l’élément* 
</dt> <dd>

Nom de l'élément.

</dd> </dl>

## <a name="remarks"></a>Remarques

Utilisez l’attribut **\[ personnalisé \]** pour définir votre propre attribut. Par exemple, vous pouvez créer un attribut à valeur de chaîne qui donne le ProgID pour une classe.

Pour récupérer une valeur d’attribut personnalisée, appelez l’un des éléments suivants :

-   ITypeLib2 :: GetCustData (rguid, pvarVal)
-   ITypeInfo2 :: GetCustData (rguid, pvarVal)
-   ITypeInfo2 :: GetFuncCustData (index, rguid, pvarVal)
-   ITypeInfo2 :: GetVarCustData (index, rguid, pVarVal)
-   ITypeInfo2 :: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**Bibliothèque**](library.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**universel**](uuid.md)
</dt> </dl>

 

 