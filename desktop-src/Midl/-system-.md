---
title: /commutateur système
description: Le commutateur/système indique au compilateur MIDL de générer une bibliothèque de types pour le système spécifié. La valeur par défaut est le système d’exploitation actuel.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /commutateur du système MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312655"
---
# <a name="system-switch"></a>/<system> Utilisez

Le **/<system>** commutateur indique au compilateur MIDL de générer une bibliothèque de types pour le système spécifié. La valeur par défaut est le système d’exploitation actuel.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * * *


</dt> <dd>

Environnement Windows 64 bits basé sur Intel, tel que Windows 2000, Windows Server 2003, Windows XP Professionnel Édition x64, Windows Vista ou Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * * *


</dt> <dd>

Un environnement Windows 64 bits basé sur des micro-appareils américain, tel que Windows 2000, Windows Server 2003, Windows XP Professionnel Édition x64, Windows Vista ou Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Le **/<system>** commutateur est fonctionnellement identique à l’option de MIDL [**/env**](-env.md) et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec mktyplib. Si vous générez un nouveau Makefile, utilisez le commutateur **/env** .

## <a name="examples"></a>Exemples

**MIDL/Win32 NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




