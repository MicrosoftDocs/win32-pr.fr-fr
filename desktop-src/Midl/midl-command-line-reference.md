---
title: Référence de Command-Line MIDL
description: Cette section contient des informations de référence pour chaque commutateur de ligne de commande et option de commutateur reconnue par le compilateur Microsoft RPC MIDL.
ms.assetid: a0e5efb0-a704-4dc5-bd7e-6c98466a2874
keywords:
- Microsoft Interface Definition Language MIDL, référence
- Référence de ligne de commande MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1569e29daf8a2976379576a5f1671f5117e7990c
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "106514262"
---
# <a name="midl-command-line-reference"></a>Référence de Command-Line MIDL

Cette section contient des informations de référence pour chaque commutateur de ligne de commande et option de commutateur reconnue par le compilateur Microsoft RPC MIDL. Les entrées de commutateur sont organisées par ordre alphabétique. La [syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md) décrit la syntaxe générale de la ligne de commande.

<dl>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)  
[Commande fichier réponse](the-response-file-command.md)  
[**/acf**](-acf.md)  
[**/align**](-align.md)  
[**/amd64**](-amd64.md)  
[**configuration de/App \_**](-app-config.md)  
[\_compatibilité/Backward](-backward-compat.md)  
[**/c \_ ext**](-c-ext.md)  
[**/caux**](-caux.md)  
[**/Char**](-char.md)  
[**/client**](-client.md)  
[**/confirm**](-confirm.md)  
[**/CPP \_ cmd**](-cpp-cmd.md)  
[**/CPP \_ opt**](-cpp-opt.md)  
[**/cstruct_out**](-cstruct-out.md) 
 [ **/cstub**](-cstub.md)  
[**/D**](-d.md)  
[**/dlldata**](-dlldata.md)  
[**/env**](-env.md)  
[**/Error**](-error.md)  
[**/Error**](-error.md)  
[**/h**](-h.md)  
[**/Header**](-header.md)  
[**/Help (/ ?)**](-help-.md)  
[**/ia64**](-ia64.md)  
[**/I**](-i.md)  
[**/IID**](-iid.md)  
[**/Import**](-import.md)  
[**/LCID**](-lcid.md)  
[**/mktyplib203**](-mktyplib203.md)  
[**/ms. \_ ext**](-ms-ext.md)  
[**/ms. \_ Union**](-ms-union.md)  
[**/MSC \_ ver**](-msc-ver.md)  
[**/New**](-new.md)  
[**/newtlb**](-newtlb.md)  
[**/non \_ CPP,/nocpp**](-no-cpp-nocpp.md)  
[**/non \_ par défaut \_ EPV**](-no-default-epv.md)  
[**/non \_ Def \_ idir**](-no-def-idir.md)  
[**/non \_ format \_ opt**](-no-format-opt.md)  
[**/non \_ robuste**](-no-robust.md)  
[**/non \_ Avertissement**](-no-warn.md)  
[**/nologo**](-nologo.md)  
[**/notlb**](-notlb.md)  
[**/o**](-o.md)  
[**/OI**](-oi.md)  
[**/Old**](-old.md)  
[**/oldtlb**](-oldtlb.md)  
[**/oldnames**](-oldnames.md)  
[**/OS**](-os.md)  
[**/osf**](-osf.md)  
[**/out**](-out.md)  
[**/Pack**](-pack.md)  
[**/prefix**](-prefix.md)  
[**/Protocol**](-protocol.md)  
[**/proxy**](-proxy.md)  
[**/Robust**](-robust.md)  
[**/rpcss**](-rpcss.md)  
[**/sal**](-sal.md)  
[**/SAL \_ local**](-sal-local.md)  
[**/saux**](-saux.md)  
[**/savePP**](-savepp.md)  
[**/sstub**](-sstub.md)  
[**vérification de/Syntax \_**](-syntax-check.md)  
[**/<system>**](-system-.md)  
[**/Target**](-target.md)  
[**/TLB**](-tlb.md)  
[**/U.**](-u.md)  
[**/Utilisez \_ EPV**](-use-epv.md)  
[**\_horodatage/version**](-version-stamp.md)  
[**/W**](-w.md)  
[**/WARN**](-warn.md)  
[**/win32**](-win32.md)  
[**/win64**](-win64.md)  
[**/WX**](-wx.md)  
[**/ZP**](-zp.md)  
[**/ZS**](-zs.md)  
</dl>

Le compilateur MIDL peut générer du code pour différentes plateformes et versions système. Consultez le commutateur [**/target**](-target.md) pour en savoir plus sur les commutateurs suggérés et sur la façon de générer du code optimisé pour une version donnée.

Notez que le signe moins (–) peut remplacer la barre oblique (/) dans tous les commutateurs de ligne de commande MIDL qui commencent par une barre oblique (/). L’exemple suivant illustre leur équivalence lors de l’appel du compilateur MIDL.

## <a name="examples"></a>Exemples

**MIDL/ACF mon nom de fichier \_ ACF. ACF** ** * *. idl**

**MIDL-ACF My \_ ACF. ACF** *filename * * *. idl**

 

 




