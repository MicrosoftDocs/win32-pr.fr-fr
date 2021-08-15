---
title: pragma (attribut)
description: La directive \ pragma MIDL \_ echo indique à MIDL d’émettre la chaîne spécifiée, sans les caractères de guillemets, dans le fichier d’en-tête généré.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma, attribut MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ca869acddf4b0a0a098707833e889efcfccc267a3abf1949921c550cf66c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383497"
---
# <a name="pragma-attribute"></a>pragma (attribut)

La \# directive **pragma MIDL \_ echo** indique à MIDL d’émettre la chaîne spécifiée, sans les caractères de guillemets, dans le fichier d’en-tête généré.

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*string* 
</dt> <dd>

Spécifie une chaîne insérée dans le fichier d’en-tête généré. Les guillemets sont supprimés pendant le processus d’insertion.

</dd> <dt>

*séquence de jetons* 
</dt> <dd>

Spécifie une séquence de jetons insérés dans le fichier d’en-tête généré dans le cadre d’une directive **\# pragma** sans traitement par le compilateur MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Spécifie la taille actuelle du Pack. Les valeurs valides sont 1, 2, 4, 8 et 16.

</dd> <dt>

*id* 
</dt> <dd>

Spécifie l’identificateur de l’utilisateur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les directives de prétraitement du langage c qui s’affichent dans le fichier IDL sont traitées par le préprocesseur du compilateur C. Les directives de **\# définition** dans le fichier IDL sont disponibles pendant la compilation MIDL, mais pas pour le compilateur C.

Par exemple, quand le préprocesseur rencontre la directive « \# définir Windows 4 », le préprocesseur remplace toutes les occurrences de « Windows » dans le fichier IDL par « 4 ». Le symbole « WINDOWS » n’est pas disponible au moment de la compilation C.

Pour permettre aux définitions de macros de préprocesseur C de passer par le compilateur MIDL au compilateur C, utilisez la directive **\# pragma MIDL \_ echo** ou le [**\_ guillemet RPC**](cpp-quote.md) . Ces directives indiquent au compilateur MIDL de générer un fichier d’en-tête qui contient la chaîne de paramètre avec les guillemets supprimés. Les directives **\# pragma MIDL \_ echo** et **CPP des \_ guillemets** sont équivalentes.

La directive **\# pragma Pack** est utilisée par le compilateur MIDL pour contrôler le compactage des structures. Il remplace le commutateur de ligne de commande [**/ZP**](-zp.md) . L’option Pack (*n*) définit la taille actuelle du Pack sur une valeur spécifique : 1, 2, 4, 8 ou 16. Les options Pack (push) et Pack (POP) présentent les caractéristiques suivantes :

-   Le compilateur gère une pile de compression. Les éléments de la pile de compression incluent une taille de Pack et un *ID* facultatif. La pile est limitée uniquement par la mémoire disponible avec la taille de Pack actuelle en haut de la pile.
-   Les résultats de Pack (push) ont fait l’objet d’un push vers la pile de compression. La pile est limitée par la mémoire disponible.
-   Pack (push,*n*) est identique à Pack (push) suivi de Pack (*n*).
-   Pack (push, *ID*) envoie également l' *ID* vers la pile de compression avec la taille de Pack.
-   Pack (push, *ID*, *n*) est identique à Pack (push, *ID*) suivi de Pack (*n*).
-   Pack (POP) génère un pop de la pile de compression. Les pop déséquilibrés provoquent des avertissements et définissent la taille actuelle du Pack à la valeur de la ligne de commande.
-   Si Pack (pop, *ID*, *n*) est spécifié, *n* est ignoré.

Le compilateur MIDL place les chaînes spécifiées dans les directives de [**\\ \_ guillemet**](cpp-quote.md) et de **pragma** cpp dans le fichier d’en-tête dans l’ordre dans lequel elles sont spécifiées dans le fichier IDL et relatives à d’autres composants d’interface dans le fichier IDL. Les chaînes doivent généralement apparaître dans la section du corps de l’interface du fichier IDL après toutes les opérations d' [**importation**](import.md) .

Le compilateur MIDL ne tente pas de traiter les directives **\# pragma** qui ne commencent pas par le préfixe « MIDL » \_ . Les autres directives **\# pragma** du fichier IDL sont passées dans le fichier d’en-tête généré sans modification.

## <a name="examples"></a>Exemples

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Devis CPP**](cpp-quote.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**port**](import.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




