---
title: Génération des fichiers stub
description: Après avoir défini l’interface client/serveur, vous développez généralement vos fichiers source client et serveur.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Appel de procédure distante RPC, tâches, génération de fichiers stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194239"
---
# <a name="generating-the-stub-files"></a>Génération des fichiers stub

Après avoir défini l’interface client/serveur, vous développez généralement vos fichiers source client et serveur. Utilisez ensuite un Makefile unique pour générer les fichiers stub et d’en-tête. Compilez et liez les applications clientes et serveur. Toutefois, s’il s’agit de votre première exposition à l’environnement informatique distribué, vous souhaiterez peut-être appeler le compilateur MIDL maintenant pour voir ce que MIDL génère avant de continuer. Le compilateur MIDL (Midl.exe) est installé automatiquement lorsque vous installez le kit de développement logiciel (SDK) de la plateforme.

Quand vous compilez ces fichiers, assurez-vous que Hello. idl et Hello. ACF se trouvent dans le même répertoire. La commande suivante génère le fichier d’en-tête Hello. h et les stubs client et serveur, Hello \_ c. c et Hello \_ s.c.

**MIDL Hello. idl**

Notez que Hello. h contient des prototypes de fonction pour HelloProc et Shutdown, ainsi que des déclarations anticipées pour deux fonctions de gestion de la mémoire, l' **\_ \_ allocation d’utilisateur MIDL** et l' **\_ utilisateur MIDL \_ gratuit**. Vous allez fournir ces deux fonctions dans l’application serveur. Si les données ont été transmises du serveur au client (au moyen d’un paramètre \[ **out** \] ), vous devez également fournir ces deux fonctions de gestion de la mémoire dans l’application cliente.

Notez les définitions de la variable de handle globale, de Hello \_ IfHandle et des noms des handles du client et de l’interface serveur, Hello \_ v1 \_ 0 \_ c \_ ifspec et Hello \_ v1 \_ 0 \_ s \_ ifspec. Les applications clientes et serveur utilisent les noms des handles d’interface dans les appels au moment de l’exécution.

À ce stade, vous n’avez rien à faire avec les fichiers stub Hello \_ c. c et Hello \_ s.c.

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

 

 




