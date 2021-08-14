---
title: Vérification des options de préprocesseur
description: Le compilateur MIDL appelle implicitement le préprocesseur et n’affiche pas ses commutateurs de préprocesseur.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL du compilateur MIDL, vérification des options du préprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9f5055623a44e88ed57b5ed0cadd0034c6962e160a081c7a55a9a51ca9e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382762"
---
# <a name="verifying-preprocessor-options"></a>Vérification des options de préprocesseur

Le compilateur MIDL appelle implicitement le préprocesseur et n’affiche pas ses commutateurs de préprocesseur. En l’absence du commutateur MIDL [**/CPP \_ OPT**](-cpp-opt.md) , la ligne de commande du préprocesseur est composée de tous les commutateurs [**/I**](-i.md), [**/d**](-d.md) et [**/u**](-u.md) utilisés dans la ligne de commande MIDL, ainsi que des commutateurs **/e** et [**/nologo**](-nologo.md) . Pour voir les commutateurs passés au préprocesseur, utilisez le commutateur [**/Confirm**](-confirm.md) du compilateur.

Par exemple, la ligne suivante :

**midl.exe-D \_ Win32 \_ winnt = 0x501-Solid-DNTENV = 1-ID : \\ NT \\ public \\ SDK \\ Inc-Confirm-Oicf-env Win32-out x86 stub. idl**

produit la sortie suivante :

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




