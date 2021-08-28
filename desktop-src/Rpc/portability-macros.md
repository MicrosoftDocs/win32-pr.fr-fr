---
title: Macros de portabilité (RPC. h)
description: Les outils RPC permettent d’obtenir l’indépendance de modèle, d’appel et de convention d’affectation de noms en associant les types de données et les types de retour de fonction dans les fichiers stub générés et les fichiers d’en-tête avec des définitions spécifiques à chaque plateforme.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Macros de portabilité RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20aa6ebda92d7c3998082fdbb5e5f07aa1be22f37a6ec65a8e81327b8614565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019223"
---
# <a name="portability-macros"></a>Macros de portabilité

Les outils RPC permettent d’obtenir l’indépendance de modèle, d’appel et de convention d’affectation de noms en associant les types de données et les types de retour de fonction dans les fichiers stub générés et les fichiers d’en-tête avec des définitions spécifiques à chaque plateforme. Ces définitions de macros garantissent que tous les types de données et fonctions qui requièrent la désignation de **\_ \_ Far** sont spécifiés en tant qu’objets Far.

L’illustration suivante montre les définitions de macros que le compilateur MIDL applique aux appels de fonction entre les composants RPC :

![Diagramme montrant les définitions de macros MIDL s’applique aux appels de fonction.](images/prog-a29.png)

Les macros RPC sont définies comme suit.



| Définition    | Description                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_\_API RPC  | Appliqué aux appels effectués par le stub à l’application utilisateur. Les deux fonctions se trouvent dans le même programme exécutable.                                       |
| \_\_RPC \_ Far  | Appliqué à la définition de macro standard pour les pointeurs. Cette définition de macro doit apparaître dans la signature de toutes les fonctions fournies par l’utilisateur. |
| \_\_\_stub RPC | Appliqué aux appels effectués à partir de la bibliothèque Runtime vers le stub. Ces appels peuvent être considérés comme privés.                                                 |
| \_\_\_utilisateur RPC | Appliqué aux appels effectués par la bibliothèque Runtime à l’application utilisateur. Ils traversent la limite entre une DLL et une application.                   |
| \_entrée RPC    | Appliqué aux appels effectués par l’application ou le stub à la bibliothèque Runtime. Cette définition de macro est appliquée à toutes les fonctions runtime RPC.           |



 

Pour établir une liaison correcte avec les bibliothèques Runtime Microsoft RPC, les stubs et les routines de prise en charge, certaines fonctions fournies par l’utilisateur doivent également inclure ces macros dans la définition de fonction. Utilisez l' **\_ \_ \_ API RPC** de macro lorsque vous définissez les fonctions associées à la gestion de la mémoire, aux handles de liaison définis par l’utilisateur et à l’attribut **transmit \_ As** , et utilisez l' **\_ \_ \_ utilisateur RPC** de la macro quand vous définissez la routine d’exécution de contexte associée au handle de contexte. Spécifiez les fonctions comme suit :

<dl> <dt>

<span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_Utilisateur \_ RPC *MIDL \_* \_ allouer (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_Utilisateur \_ RPC *utilisateur \_* \_ gratuit (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_\_Liaison *comme HandleType* de l’utilisateur RPC \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_\_ *Comme HANDLETYPE* utilisateur RPC \_ annuler la liaison (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Type* d’utilisateur RPC \_ sur \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Type* \_ d’utilisateur RPC \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Type d’utilisateur RPC \_ à transmission \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Type* d’utilisateur RPC de la transmission \_ de transmission \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_ *Type* d’utilisateur RPC \_ gratuit \_ local
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Type* d’utilisateur RPC \_ gratuit \_ inst (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_Transmission \_ libre du *type* d’utilisateur RPC \_ \_ (...)
</dt> <dd></dd> <dt>

<span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_Arrêt du contexte de l’utilisateur RPC \_ (...)
</dt> <dd></dd> </dl>

> [!Note]  
> Tous les paramètres de pointeur dans ces fonctions doivent être spécifiés à l’aide de la macro **\_ \_ RPC \_ bien**.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



 

 





