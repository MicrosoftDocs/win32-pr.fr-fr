---
title: Commutateur/d
description: Le commutateur/D définit un nom et une valeur facultative à passer au préprocesseur C comme s’il s’agissait d’une directive \ define. Plusieurs directives/D peuvent être utilisées dans une ligne de commande.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- MIDL du commutateur/d
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8bc01a978949ec0f0cc4ff78289a1cb442046966f1cea954c6b65cc232f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385776"
---
# <a name="d-switch"></a>Commutateur/d

Le commutateur **/d** définit un nom et une valeur facultative à passer au préprocesseur C comme s’il s’agissait d’une directive de **\# définition** . Plusieurs directives **/d** peuvent être utilisées dans une ligne de commande.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*name* 
</dt> <dd>

Spécifie un nom défini qui est passé au préprocesseur C lorsque le commutateur [**/CPP \_ cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas présent.

</dd> <dt>

*définition* 
</dt> <dd>

Spécifie une valeur associée au nom défini.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’espace blanc entre le commutateur **/d** et le nom défini est facultatif.

Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le commutateur **/CPP \_ cmd** avec les options [**/i**](-i.md), **/d** et [**/u**](-u.md) et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF.

Le commutateur du compilateur MIDL **/d** est ignoré lorsque le commutateur du compilateur MIDL [/non \_ CPP](-no-cpp-nocpp.md) ou [**/CPP \_ OPT**](-cpp-opt.md) est spécifié.

## <a name="examples"></a>Exemples

**MIDL-DUNICODE nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/non \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U.**](-u.md)
</dt> </dl>

 

 




