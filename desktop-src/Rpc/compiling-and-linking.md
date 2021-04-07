---
title: Compilation et liaison
description: Le Makefile suivant montre les dépendances entre les fichiers nécessaires pour compiler les applications clientes et serveur, et les lier à la bibliothèque Runtime RPC et à la bibliothèque Runtime C standard.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Appel de procédure distante RPC, tâches, compilation et liaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940026"
---
# <a name="compiling-and-linking"></a><span data-ttu-id="4a063-104">Compilation et liaison</span><span class="sxs-lookup"><span data-stu-id="4a063-104">Compiling and Linking</span></span>

<span data-ttu-id="4a063-105">Le Makefile suivant montre les dépendances entre les fichiers nécessaires pour compiler les applications clientes et serveur, et les lier à la bibliothèque Runtime RPC et à la bibliothèque Runtime C standard.</span><span class="sxs-lookup"><span data-stu-id="4a063-105">The following makefile shows the dependencies among the files needed to compile the client and server applications and link them to the RPC run-time library and the standard C run-time library.</span></span>

<span data-ttu-id="4a063-106">Ce makefile peut être utilisé pour générer des applications clientes et serveur à partir du code source de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="4a063-106">This makefile can be used to build client and server applications from the source code in this tutorial.</span></span> <span data-ttu-id="4a063-107">Les stubs et les en-têtes indiqués ici ont été générés avec MIDL version 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a063-107">The stubs and headers shown here were generated with MIDL version 2.0.</span></span> <span data-ttu-id="4a063-108">Les commandes et les arguments du compilateur et de l’éditeur de liens peuvent être différents pour la configuration de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4a063-108">The compiler and linker commands and arguments may be different for your computer configuration.</span></span> <span data-ttu-id="4a063-109">Pour plus d’informations, consultez la documentation de votre compilateur.</span><span class="sxs-lookup"><span data-stu-id="4a063-109">See your compiler documentation for more information.</span></span>

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

 

 




