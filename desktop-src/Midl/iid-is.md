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
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383866"
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

## <a name="remarks"></a>Remarques

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

[**dessin**](object.md)
</dt> <dt>

[**universel**](uuid.md)
</dt> </dl>

 

 




