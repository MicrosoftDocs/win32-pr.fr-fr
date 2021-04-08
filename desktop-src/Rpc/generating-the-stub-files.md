---
title: Génération des fichiers stub
description: Après avoir défini l’interface client/serveur, vous développez généralement vos fichiers source client et serveur.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Appel de procédure distante RPC, tâches, génération de fichiers stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839953"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="753bb-104">Génération des fichiers stub</span><span class="sxs-lookup"><span data-stu-id="753bb-104">Generating the Stub Files</span></span>

<span data-ttu-id="753bb-105">Après avoir défini l’interface client/serveur, vous développez généralement vos fichiers source client et serveur.</span><span class="sxs-lookup"><span data-stu-id="753bb-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="753bb-106">Utilisez ensuite un Makefile unique pour générer les fichiers stub et d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="753bb-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="753bb-107">Compilez et liez les applications clientes et serveur.</span><span class="sxs-lookup"><span data-stu-id="753bb-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="753bb-108">Toutefois, s’il s’agit de votre première exposition à l’environnement informatique distribué, vous souhaiterez peut-être appeler le compilateur MIDL maintenant pour voir ce que MIDL génère avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="753bb-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="753bb-109">Le compilateur MIDL (Midl.exe) est installé automatiquement lorsque vous installez le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="753bb-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="753bb-110">Quand vous compilez ces fichiers, assurez-vous que Hello. idl et Hello. ACF se trouvent dans le même répertoire.</span><span class="sxs-lookup"><span data-stu-id="753bb-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="753bb-111">La commande suivante génère le fichier d’en-tête Hello. h et les stubs client et serveur, Hello \_ c. c et Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="753bb-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="753bb-112">**MIDL Hello. idl**</span><span class="sxs-lookup"><span data-stu-id="753bb-112">**midl hello.idl**</span></span>

<span data-ttu-id="753bb-113">Notez que Hello. h contient des prototypes de fonction pour HelloProc et Shutdown, ainsi que des déclarations anticipées pour deux fonctions de gestion de la mémoire, l' **\_ \_ allocation d’utilisateur MIDL** et l' **\_ utilisateur MIDL \_ gratuit**.</span><span class="sxs-lookup"><span data-stu-id="753bb-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="753bb-114">Vous allez fournir ces deux fonctions dans l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="753bb-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="753bb-115">Si les données ont été transmises du serveur au client (au moyen d’un paramètre \[ **out** \] ), vous devez également fournir ces deux fonctions de gestion de la mémoire dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="753bb-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="753bb-116">Notez les définitions de la variable de handle globale, de Hello \_ IfHandle et des noms des handles du client et de l’interface serveur, Hello \_ v1 \_ 0 \_ c \_ ifspec et Hello \_ v1 \_ 0 \_ s \_ ifspec.</span><span class="sxs-lookup"><span data-stu-id="753bb-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="753bb-117">Les applications clientes et serveur utilisent les noms des handles d’interface dans les appels au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="753bb-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="753bb-118">À ce stade, vous n’avez rien à faire avec les fichiers stub Hello \_ c. c et Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="753bb-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




