---
title: optional (attribut)
description: L’attribut \ Optional spécifie un paramètre facultatif pour une fonction membre.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- MIDL d’attribut facultatif
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842262"
---
# <a name="optional-attribute"></a>optional (attribut)

L’attribut **\[ facultatif \]** spécifie un paramètre facultatif pour une fonction membre.

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de retour* 
</dt> <dd>

Spécifie le type de retour de la fonction.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*autres attributs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL facultatifs.

</dd> <dt>

*type de paramètre* 
</dt> <dd>

Type de données du paramètre facultatif.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Spécifie le nom du paramètre facultatif.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ facultatif \]** est valide uniquement si le paramètre est de type **Variant** ou **Variant** \* .

Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :

1.  Paramètres obligatoires (paramètres qui n’ont pas les **\[** attributs [**DefaultValue**](defaultvalue.md) **\]** ou **\[ facultatifs \]** )
2.  Paramètres facultatifs avec ou sans l' **\[** [](defaultvalue.md) **\]** attribut DefaultValue,
3.  Paramètres avec l’attribut **\[ facultatif \]** et sans l' **\[** attribut [**DefaultValue**](defaultvalue.md) **\]** ,
4.  **\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant,
5.  **\[**[**retVal**](retval.md) **\]** paramètre

Vous ne pouvez pas appliquer l’attribut **\[ facultatif \]** à un paramètre qui possède également les **\[** [](lcid.md) **\]** attributs LCID ou **\[** [**retVal**](retval.md) **\]** .

## <a name="examples"></a>Exemples

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DefaultValue**](defaultvalue.md)
</dt> <dt>

[Génération d’une bibliothèque de types avec MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[Exemple de fichier ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Syntaxe du fichier ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> </dl>

 

 