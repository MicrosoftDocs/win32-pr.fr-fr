---
title: in (attribut)
description: L’attribut \ in \ indique qu’un paramètre doit être passé de la procédure appelante à la procédure appelée.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- dans l’attribut MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726965"
---
# <a name="in-attribute"></a>in (attribut)

L’attribut **\[ in \]** indique qu’un paramètre doit être passé de la procédure appelante à la procédure appelée.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides sont **\[ callback \]**, **\[ local \]**, attribut de pointeur **\[ Ref \]**, **\[ unique \]** ou **\[ ptr \]**, et les attributs d’utilisation **\[ chaîne \]**, **\[ Ignorer \]** et **\[ \_ handle \] de contexte**.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type de **base \_**, un [**struct**](struct.md), une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*pointeur-déclarateur* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est le même que le déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**const**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre spécifié. Les attributs de paramètre avec l’attribut in peuvent également prendre l' **\[ \] attribut directionnel**, les attributs **\[ de \]** **\[ \]** **\[ \]** **\[ \_ \]** champ en **\[ premier \_ \]** **\[ \]** **\[ \]** **\[ \_ \] ,,** le nom, la **\[ longueur \_ est \]**, le **\[ nombre maximal \_ \]**, la **\[ taille \_ et le type de commutateur, l’attribut de pointeur REF, unique ou PTR ; et le handle de contexte et la chaîne des attributs d’utilisation. \]** **\[ \_ \]** L’attribut d’utilisation **\[ ignore \]** ne peut pas être utilisé en tant qu’attribut de paramètre. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*declarator* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ in \]** a un attribut réciproque, **\[** [**out**](out-idl.md) **\]** , qui indique qu’un paramètre doit être retourné à partir de la procédure appelée à la procédure appelante. Les attributs in et **\[ out \]** sont appelés attributs **\[ de \]** paramètres directionnels, car ils spécifient la direction dans laquelle les paramètres sont passés. Un paramètre peut être défini comme **\[ in \]**, **\[ out \]** ou **\[ in**, **out \]**.

L’attribut **\[ in \]** identifie les paramètres qui sont marshalés par le stub client pour la transmission au serveur.

L’attribut in est appliqué à un paramètre par défaut quand aucun attribut **\[ de \]** paramètre directionnel n’est spécifié.

## <a name="examples"></a>Exemples

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**allouer un \_ utilisateur MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**à**](out-idl.md)
</dt> </dl>

 

 