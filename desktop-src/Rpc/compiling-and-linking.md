---
title: Compilation et liaison
description: Le Makefile suivant montre les dépendances entre les fichiers nécessaires pour compiler les applications clientes et serveur, et les lier à la bibliothèque Runtime RPC et à la bibliothèque Runtime C standard.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Appel de procédure distante RPC, tâches, compilation et liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2500a763db149eca914060dd7920548883fa57fbd5642485a41f5a55c65cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931712"
---
# <a name="compiling-and-linking"></a>Compilation et liaison

Le Makefile suivant montre les dépendances entre les fichiers nécessaires pour compiler les applications clientes et serveur, et les lier à la bibliothèque Runtime RPC et à la bibliothèque Runtime C standard.

Ce makefile peut être utilisé pour générer des applications clientes et serveur à partir du code source de ce didacticiel. Les stubs et les en-têtes indiqués ici ont été générés avec MIDL version 2,0. Les commandes et les arguments du compilateur et de l’éditeur de liens peuvent être différents pour la configuration de votre ordinateur. Pour plus d’informations, consultez la documentation de votre compilateur.

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




