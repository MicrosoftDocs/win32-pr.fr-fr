---
title: commutateur/env
description: Le commutateur/env sélectionne l’environnement dans lequel l’application s’exécute.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL du commutateur/env
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381824"
---
# <a name="env-switch"></a>commutateur/env

Le commutateur **/env** sélectionne l’environnement dans lequel l’application s’exécute.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 32 bits.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * * *


</dt> <dd>

Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement Intel architecture 64 bits (IA64).

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * * *


</dt> <dd>

Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement Advanced Micro Devices 64 bits (AMD64).

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * * *


</dt> <dd>

Même comportement que *ia64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Le commutateur **/env** affecte principalement le niveau de compression utilisé pour les structures dans cet environnement. Veillez à spécifier le même paramètre de niveau d’empaquetage pour le compilateur MIDL et le compilateur C.

Le commutateur **/env** détermine le niveau de compression et d’autres paramètres comme suit :

-   Lorsque vous spécifiez **Win32**, les stubs générés utilisent le niveau de compactage du compilateur C 8 pour tous les types impliqués dans les opérations distantes. Les types de données [**int**](int.md) sont à la fois 32 bits. Les pointeurs sont 32 bits.
-   Lorsque vous spécifiez **ia64** ou **amd64**, le compilateur MIDL s’exécute en mode cross-compiler pour la plateforme (Intel ou AMD) 64 bits indiquée. Les stubs générés utilisent le niveau de compactage du compilateur C 8 pour tous les types impliqués dans les opérations distantes. Les types de données [**long**](long.md) et [**int**](int.md) sont 32 bits. Les pointeurs sont 64 bits.

Les commutateurs [**/align**](-align.md), [**/Pack**](-pack.md)et [**/ZP**](-zp.md) ont la priorité sur les paramètres **/env** .

Pour plus d’informations sur la prise en charge de 64 bits pour MIDL et RPC, consultez [conception d’interfaces compatibles avec 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Exemples

**MIDL/env Win32 nom_fichier. idl**

**MIDL/env ia64 NomFichier. idl**

**MIDL/env fichier amd64. idl**

**MIDL/env Win64 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 