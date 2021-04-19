---
title: attribut de plage
description: L’attribut \ Range \ vous permet de spécifier une plage de valeurs autorisées pour les arguments ou les champs dont les valeurs sont définies au moment de l’exécution. Lorsqu’il est utilisé avec un type de canal, l’attribut spécifie la plage autorisée pour le nombre d’éléments dans les segments de canal.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- attribut de plage MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512723"
---
# <a name="range-attribute"></a>attribut de plage

L’attribut **\[ Range \]** vous permet de spécifier une plage de valeurs autorisées pour les arguments ou les champs dont les valeurs sont définies au moment de l’exécution. Lorsqu’il est utilisé avec un type de canal, l’attribut spécifie la plage autorisée pour le nombre d’éléments dans les segments de canal.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*faible Val* 
</dt> <dd>

Valeur autorisée la plus basse que le paramètre ou le champ peut contenir.

</dd> <dt>

*haute-Val* 
</dt> <dd>

Valeur autorisée la plus élevée que le paramètre ou le champ peut contenir.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Type intégral autre que [**hyper**](hyper.md) ou [**\_ \_ Int64**](--int64.md), un identificateur de type à un type intégral, un type [**enum**](enum.md) ou un nom de type de canal.

</dd> <dt>

*declarator* 
</dt> <dd>

Déclarateur C standard, tel qu’un identificateur.

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez l’attribut **\[ Range \]** pour modifier la signification des paramètres ou des champs sensibles, tels que ceux utilisés pour la taille ou la longueur, avec des tableaux conformes ou variables, ou chaque fois que vous souhaitez vérifier un paramètre ou une valeur de champ par rapport à une plage de valeurs valides. L’attribut s’applique aux paramètres de niveau supérieur, ainsi qu’aux paramètres et champs de niveau inférieur. L’ajout de l’attribut de **\[ plage \]** à un type ne change pas son format de câble, donc n’affecte pas la compatibilité descendante.

L’attribut **\[ Range \]** peut également être utilisé sur des données conformes, telles que des mémoires tampons ou des tableaux, avec un attribut de conformité. L’effet est de limiter toutes les tailles de conformité pour les données conformes à la plage spécifiée. Si les données conformes sont un tableau multidimensionnel, chaque dimension de tableau est limitée à la plage spécifiée.

L’utilisation de **\[ Range \]** sur des données conformes nécessite que la cible de compilation soit â «Target nt60 ou version ultérieure.

Notez que vous devez utiliser l’option du compilateur [**/Robust**](-robust.md) quand vous compilez votre fichier IDL afin de générer le code stub qui effectuera ces vérifications. Sans le commutateur **/Robust** , le compilateur MIDL ignore cet attribut.

## <a name="examples"></a>Exemples

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Tableaux](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**tout d’abord, \_**](first-is.md)
</dt> <dt>

[**la dernière \_ est**](last-is.md)
</dt> <dt>

[**la longueur \_ est**](length-is.md)
</dt> <dt>

[**le nombre maximal \_ est**](max-is.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**la taille \_ est**](size-is.md)
</dt> <dt>

[**le commutateur \_ est**](switch-is.md)
</dt> </dl>

 

 