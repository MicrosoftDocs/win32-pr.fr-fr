---
title: attribut force_allocate
description: L’attribut ACF \ force \_ allocate \ force l’allocation d’un paramètre de pointeur à l’aide \_ de l’allocation d’utilisateur MIDL \_ au lieu d’optimiser l’allocation.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093586"
---
# <a name="force_allocate-attribute"></a>forcer l’allocation de l' \_ attribut

L’attribut ACF \[ **force \_ allocate** \] force un paramètre de pointeur à être alloué à l’aide de l’allocation d' [**\_ utilisateur \_ MIDL**](midl-user-allocate-1.md) au lieu d’optimiser l’allocation.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Paramètres

Cet attribut n’a aucun paramètre.

## <a name="remarks"></a>Notes

RPC tente de réduire les allocations de mémoire sur le serveur en fournissant des pointeurs aux mémoires tampons de mémoire internes. Cette approche peut provoquer des problèmes pour les applications qui tentent d’appeler directement l' [**\_ utilisateur MIDL \_**](midl-user-free-1.md) sur les pointeurs fournis par RPC, car un pointeur qui a été optimisé ne peut pas être libéré. Le marquage d’un paramètre avec l' **\[ \_ allocation \] forcée** empêche cette optimisation pour tous les pointeurs qui le dérivent.

Une autre utilisation courante de **\[ force \_ allocate \]** consiste à garantir l’alignement de la mémoire vers laquelle pointe la mémoire si une application requiert un alignement supérieur à celui de la mémoire vers laquelle pointe. Par exemple, les applications transmettent souvent des données dans un tableau générique d’octets plutôt que d’utiliser le type réel, mais l’alignement d’un octet est garanti uniquement à 1, ce qui peut entraîner des problèmes pour les applications qui supposent un plus grand alignement. En marquant le paramètre avec **\[ force \_ allocate \]**, l’application peut garantir que toute la mémoire pointée aura un alignement égal à celui garanti par l' [**\_ \_ allocation d’utilisateur MIDL**](midl-user-allocate-1.md).

## <a name="examples"></a>Exemples

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éviter le masquage des informations](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Conception d’interfaces compatibles 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**allouer un \_ utilisateur MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**\_utilisateur \_ gratuit MIDL**](midl-user-free-1.md)
</dt> <dt>

[**lui**](allocate.md)
</dt> </dl>

 

 