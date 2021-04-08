---
title: annoter l’attribut
description: L’attribut \ Annotate \ vous permet de spécifier une chaîne d’annotation SAL pour la méthode, le paramètre ou le champ de structure spécifié.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- annoter l’attribut MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732085"
---
# <a name="annotate-attribute"></a>annoter l’attribut

L’attribut **\[ annotation \]** vous permet de spécifier une chaîne d’annotation SAL pour la méthode, le paramètre ou le champ de structure spécifié.

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*string* 
</dt> <dd>

Chaîne d’annotation SAL spécifiée.

</dd> <dt>

*function-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs qui s’appliquent à la fonction. Les attributs de fonction valides incluent le [**\[ \] rappel**](callback.md); les attributs de pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ chaîne \]**](string.md), [**\[ Ignorer \]**](ignore.md)et [**\[ \_ handle \] de contexte**](context-handle.md). Plusieurs attributs doivent être séparés par des virgules.

</dd> <dt>

*déclarateur de fonction* 
</dt> <dd>

Spécifie le spécificateur de type, le nom de fonction et la liste de paramètres pour la fonction.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Spécifie un type de **base \_**, un [**\[ struct \]**](struct.md), une [**Union**](union.md)ou un type [**\[ enum \]**](enum.md) ou un identificateur de type. Une spécification de stockage facultative peut précéder *le type-specifier*.

</dd> <dt>

*pointeur-déclarateur* 
</dt> <dd>

Spécifie zéro ou plusieurs déclarateurs de pointeur. Un déclarateur de pointeur est identique à un déclarateur de pointeur utilisé dans C ; elle est construite à partir de l' \* indicateur, de modificateurs tels que **Far** et de l’identificateur [**\[ const \]**](const.md).

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Spécifie le nom de la procédure distante.

</dd> <dt>

*Parameter-attribute-List* 
</dt> <dd>

Spécifie zéro, un ou plusieurs attributs appropriés pour le type de paramètre. Les attributs de paramètre avec l’attribut in peuvent également prendre l' [**\[ attribut \] directionnel. les**](out-idl.md)attributs de champ [**\[ \_ sont \]**](first-is.md), [**\[ Last \_ \] is**](last-is.md), [**\[ Length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)et [**\[ Switch \_ type \]**](switch-type.md); les attributs [**\[ de \]**](in.md) pointeur [**\[ Ref \]**](ref.md), [**\[ unique \]**](unique.md)ou [**\[ ptr \]**](ptr.md); et les attributs d’utilisation [**\[ \_ handle \] de contexte**](context-handle.md) et [**\[ chaîne \]**](string.md). L’attribut d’utilisation [**\[ ignore \]**](ignore.md) ne peut pas être utilisé en tant qu’attribut de paramètre. Plusieurs attributs doivent être séparés par des virgules.

</dd> <dt>

*declarator* 
</dt> <dd>

Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau. Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**\[ tableaux \]**](../rpc/arrays.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers). Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.

</dd> </dl>

## <a name="remarks"></a>Notes

L’attribut **\[ annoter \]** permet de remplacer les annotations SAL générées par MIDL ou de les ajouter à des endroits où MIDL ne génère pas explicitement d’annotation. Si [**/SAL**](-sal.md) n’est pas spécifié sur la ligne de commande, cet attribut est ignoré.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/SAL \_ local**](-sal-local.md)
</dt> </dl>

 

 