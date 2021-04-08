---
title: retval (attribut)
description: L’attribut \ retval \ désigne le paramètre qui reçoit la valeur de retour du membre.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- attribut retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842130"
---
# <a name="retval-attribute"></a>retval (attribut)

L’attribut **\[ retval \]** désigne le paramètre qui reçoit la valeur de retour du membre.

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de retour* 
</dt> <dd>

Type de données de la valeur de retour de la procédure distante.

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom utilisé pour appeler la procédure distante.

</dd> <dt>

*attributs facultatifs* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL.

</dd> <dt>

*type de données* 
</dt> <dd>

Type des données passées via le paramètre.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Nom de l’identificateur du paramètre.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser l’attribut **\[ retval \]** sur les paramètres des membres d’interface qui décrivent des méthodes ou obtiennent des propriétés. (L’attribut est requis sur le dernier paramètre d’une méthode qui a le **\[** [**propget**](propget.md) **\]** attribut.) Le paramètre doit avoir l' **\[** attribut [**out**](out-idl.md) **\]** et doit être un type pointeur.

Vous ne pouvez pas appliquer l' **\[** attribut [**facultatif**](optional.md) **\]** à un paramètre **\[ \] retVal** .

Le compilateur MIDL accepte l’ordonnancement des paramètres suivant (de gauche à droite) :

1.  Paramètres obligatoires (paramètres qui n’ont pas les **\[** attributs [**DefaultValue**](defaultvalue.md) **\]** ou **\[** [**Optional**](optional.md) **\]** ).
2.  Paramètres facultatifs avec ou sans l' **\[** [](defaultvalue.md) **\]** attribut DefaultValue.
3.  Paramètres avec l' **\[** attribut [**facultatif**](optional.md) **\]** et sans l' **\[** attribut [**DefaultValue**](defaultvalue.md) **\]** .
4.  **\[** paramètre [**LCID**](lcid.md) **\]** , le cas échéant.
5.  paramètre **\[ retval \]** .

Les paramètres avec l’attribut **\[ retval \]** ne sont pas affichés dans les navigateurs orientés utilisateur.

### <a name="flags"></a>Indicateurs

IDLFLAG \_ FRETVAL

## <a name="examples"></a>Exemples

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
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

[**facultatif**](optional.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 