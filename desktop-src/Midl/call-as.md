---
title: call_as (attribut)
description: L’attribut \ Call \_ As \ vous permet de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093738"
---
# <a name="call_as-attribute"></a>appeler \_ en tant qu’attribut

L' **\[ appel \_ en \] tant qu'** attribut vous permet de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*local-proc* 
</dt> <dd>

Spécifie une routine définie par l’opération.

</dd> <dt>

*Operation-Attribute-List* 
</dt> <dd>

Spécifie un ou plusieurs attributs qui s’appliquent à l’opération. Séparez plusieurs attributs par des virgules.

</dd> <dt>

*Operation-name* 
</dt> <dd>

Spécifie l’opération nommée présentée à l’application.

</dd> </dl>

## <a name="remarks"></a>Notes

La possibilité de mapper une fonction qui ne peut pas être appelée à distance à une fonction distante est particulièrement utile dans les interfaces qui ont de nombreux types de paramètres qui ne peuvent pas être transmis sur le réseau. Au lieu d’utiliser plusieurs types de **\[** [**représentation \_**](represent-as.md) comme **\]** et de **\[** [**transmission \_ en tant que**](transmit-as.md) **\]** types, vous pouvez combiner toutes les conversions à l’aide de routines **\[ Call \_ As \]** . Vous fournissez les deux **\[ appels \_ en tant que \]** routines (côté client et côté serveur) pour lier la routine entre les appels d’application et les appels distants.

L' **\[ appel \_ en \] tant qu'** attribut peut être utilisé pour les interfaces d’objet. Dans ce cas, la définition d’interface peut être utilisée pour les appels locaux et les appels distants, car l' **\[ appel \_ de la fonction \]** autorise une interface qui n’est pas accessible à distance pour être mappée en toute transparence à une interface distante. L' **\[ appel \_ en \] tant qu'** attribut ne peut pas être utilisé avec le mode [**/OSF**](-osf.md) .

Par exemple, supposons que la routine **F1** dans l’interface d’objet **IFace** nécessite de nombreuses conversions entre les appels utilisateur et ce qui est réellement transmis. Les exemples suivants décrivent les fichiers IDL et ACF pour l’interface **IFace**:

Dans le fichier IDL de l’interface **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

Dans le ACF pour l’interface **IFace**:

``` syntax
[call_as( f1 )] Remf1();
```

Le fichier d’en-tête généré définit alors l’interface à l’aide de la définition de la **touche F1**, mais il fournit également des stubs pour **Remf1**.

Le compilateur MIDL génère le vtable suivant dans le fichier d’en-tête pour l’interface **IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

Le proxy côté client a ensuite un proxy généré par MIDL standard pour **Remf1**, tandis que le stub côté serveur pour **Remf1** est le même que le stub généré par MIDL standard :

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

Ensuite, les deux **\[ appels \_ en \] tant que** routines de liaison (côté client et côté serveur) doivent être codés manuellement :

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

Pour les interfaces d’objet, il s’agit des prototypes pour les routines de liaison.

Côté client :

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Côté serveur :

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

Pour les interfaces qui ne sont pas des objets, il s’agit des prototypes pour les routines de liaison.

Côté client :

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Côté serveur :

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**représenter \_ comme**](represent-as.md)
</dt> <dt>

[**transmettre \_ en tant que**](transmit-as.md)
</dt> </dl>

 

 




