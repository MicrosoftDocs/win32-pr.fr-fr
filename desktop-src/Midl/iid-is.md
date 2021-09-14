---
title: iid_is (attribut)
description: L’attribut \ IID \_ est \ pointeur spécifie l’IID de l’interface com vers laquelle pointe un pointeur d’interface.
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is MIDL de l’attribut
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94c6f46a6828e81817e45ff6eb6eb8245b00a61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093517"
---
# <a name="iid_is-attribute"></a>IID \_ est l’attribut

L' **\[ IID \_ est \]** l’attribut de pointeur spécifie l’IID de l’interface com vers laquelle pointe un pointeur d’interface.

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Limited-expression* 
</dt> <dd>

Spécifie une expression de langage C. Le compilateur MIDL prend en charge les expressions conditionnelles, les expressions logiques, les expressions relationnelles et les expressions arithmétiques. MIDL n’autorise pas les appels de fonction dans les expressions et n’autorise pas les opérateurs d’incrémentation et de décrémentation.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser **\[ IID \_ \]** dans les listes d’attributs pour les paramètres de fonction et pour les membres de structure ou d’Union. Les stubs utilisent l’IID pour déterminer comment marshaler le pointeur d’interface. Cela est utile pour un pointeur d’interface qui est typé comme paramètre de classe de base.

Les fichiers qui utilisent l' **\[ IID \_ sont \]** des attributs doivent être compilés avec le compilateur MIDL en mode par défaut, qui n’utilise pas le commutateur [**/OSF**](-osf.md)

## <a name="examples"></a>Exemples

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**object**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 




