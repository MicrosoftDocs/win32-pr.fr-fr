---
title: cpp_quote (attribut)
description: Le \_ mot clé du guillemet CPP demande à MIDL d’émettre la chaîne spécifiée, sans les caractères guillemets, dans le fichier d’en-tête généré.
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote MIDL de l’attribut
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093710"
---
# <a name="cpp_quote-attribute"></a>\_attribut de guillemets CPP

Le mot clé du **\_ guillemet CPP** demande à MIDL d’émettre la chaîne spécifiée, sans les caractères guillemets, dans le fichier d’en-tête généré.

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*string* 
</dt> <dd>

Spécifie une chaîne entre guillemets émise dans le fichier d’en-tête généré. La chaîne doit être placée entre guillemets pour empêcher l’extension par le préprocesseur C.

</dd> </dl>

## <a name="remarks"></a>Notes

Les directives de prétraitement du langage c qui s’affichent dans le fichier IDL sont traitées par le préprocesseur du compilateur C. Les directives de **\# définition** dans le fichier IDL sont disponibles pendant la compilation MIDL, mais ne sont pas disponibles pour le compilateur C.

Par exemple, quand le préprocesseur rencontre la directive « \# définir Windows 4 », le préprocesseur remplace toutes les occurrences de « Windows » dans le fichier IDL par « 4 ». Le symbole « WINDOWS » n’est pas disponible lors de la compilation en langage C.

Pour permettre aux définitions de macros de préprocesseur C de passer par le compilateur MIDL au compilateur C, utilisez la directive **\# pragma MIDL \_ echo** ou le **\_ guillemet RPC** . Ces directives indiquent au compilateur MIDL de générer un fichier d’en-tête qui contient la chaîne de paramètre avec les guillemets supprimés. Les directives **\# pragma MIDL \_ echo** et **CPP des \_ guillemets** sont équivalentes.

Le compilateur MIDL place les chaînes spécifiées dans les directives de **\_ guillemet** et [**pragma**](pragma.md) cpp dans le fichier d’en-tête, dans l’ordre dans lequel elles sont spécifiées dans le fichier IDL, et par rapport à d’autres composants d’interface dans le fichier IDL. Les chaînes doivent généralement apparaître dans la section corps de l’interface de fichier IDL après toutes les opérations d' [**importation**](import.md) .

## <a name="examples"></a>Exemples

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**port**](import.md)
</dt> <dt>

[**Bali**](pragma.md)
</dt> </dl>

 

 




