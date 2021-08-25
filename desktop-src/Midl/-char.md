---
title: commutateur/char
description: Le commutateur/char permet de s’assurer que le compilateur MIDL et le compilateur C fonctionnent ensemble correctement pour tous les types char et Small.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- MIDL du commutateur/char
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb459f7c2d6ff98a35e139cf07d9d95c4bed575e52b3d20258f570f07297943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963189"
---
# <a name="char-switch"></a>commutateur/char

Le commutateur **/char** permet de s’assurer que le compilateur MIDL et le compilateur C fonctionnent ensemble correctement pour tous les types [**char**](char-idl.md) et [**Small**](small.md) .

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>signé * * * * *


</dt> <dd>

Spécifie que le type de compilateur C par défaut pour [**char**](char-idl.md) est signé. Toutes les occurrences de **char** non accompagnées d’une spécification de signe sont générées en tant que type unsigned char.

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>non signé * * * *


</dt> <dd>

Spécifie que le type de compilateur C par défaut pour [**char**](char-idl.md) n’est pas signé. Toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe sont générées comme étant signées petit.

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7 * * * *


</dt> <dd>

Spécifie que toutes les valeurs [**char**](char-idl.md) doivent être passées dans les fichiers générés sans un mot clé Sign spécifique. Toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe sont générées sous une forme **réduite**.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Par définition, le [**caractère**](char-idl.md) MIDL n’est pas signé. « Small » est défini en termes de **char** ( \# define Small Char) et MIDL [**Small**](small.md) est signé.

Le commutateur **/char** indique au compilateur MIDL de spécifier des déclarations [**signées**](signed.md) ou [**non**](unsigned.md) signées explicites dans les fichiers générés lorsque la déclaration de signe du compilateur C est en conflit avec la valeur par défaut MIDL pour ce type.

N’oubliez pas que le compilateur MIDL génère les stubs en tant que code source C, que vous devez compiler dans le cadre de vos programmes client et serveur. Certains compilateurs utilisent [**des données de type char**](char-idl.md) partout **signées** , qui sont spécifiées dans le code source. Le code source stub généré par le compilateur MIDL traite toutes les données **char** comme des **caractères non signés**. Si le compilateur MIDL a simplement généré toutes les données **char** dans le fichier IDL en tant que données **char** dans les stubs, les compilateurs qui utilisent un **char signé** pour les données **char** provoqueraient un conflit dans le code source du stub.

L’objectif du commutateur de ligne de commande **/char** est de résoudre ces conflits potentiels. Elle conserve toutes les données spécifiées en tant que [**char**](char-idl.md) dans le fichier IDL en tant que **unsigned char** dans le code source stub. Il gère également les [**petites**](small.md) données comme étant signées.

Le tableau suivant récapitule les types générés.



| MIDL (option/char)       | Type char généré | Type de petite taille généré |
|-------------------------|---------------------|----------------------|
| **MIDL/char signé**   | **unsigned char**   | **small**            |
| **MIDL/char non signé** | **char**            | **signé petit**     |
| **MIDL/char ascii7**   | **char**            | **small**            |



 

L’option **/char** signed indique que les types char et Small du compilateur C sont signés. Pour correspondre à la valeur par défaut MIDL pour **char**, le compilateur MIDL doit convertir toutes les utilisations de **char** non accompagnées d’une spécification de signe en **char non signé**. Le [**petit**](small.md) type n’est pas modifié, car la valeur par défaut de ce compilateur C correspond à la valeur par défaut MIDL pour **Small**.

L’option non signée **/char** indique que le type de [**caractère**](char-idl.md) du compilateur C n’est pas signé. Le compilateur MIDL convertit toutes les utilisations de [**Small**](small.md) non accompagnées d’une spécification de signe à une **signature** de **petite taille**.

L’option ascii7 indique qu’aucune spécification de signe explicite n’est ajoutée aux types [**char**](char-idl.md) . Le type [**petit**](small.md) est généré en tant que **petit**.

Pour éviter toute confusion, vous devez utiliser des spécifications de signe explicite pour les types [**char**](char-idl.md) et Small dans la mesure du possible dans le fichier IDL. Notez que l’utilisation de types de **caractères** signés de manière explicite dans votre fichier IDL n’est pas prise en charge par l’IDL DCE. Par conséquent, cette fonctionnalité n’est pas disponible quand vous compilez avec le commutateur MIDL [**/OSF**](-osf.md) .

Pour plus d’informations sur **/char**, consultez [**petit**](small.md).

## <a name="examples"></a>Exemples

**MIDL/char signé nom de fichier. idl**

**MIDL/char unsigned filename. idl**

**MIDL/char ascii7 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Small**](small.md)
</dt> </dl>

 

 




