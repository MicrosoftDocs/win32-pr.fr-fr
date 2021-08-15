---
title: RPC_IF_HANDLE (rpcdce. h)
description: Le \_ type de données RPC if \_ handle déclare un handle d’interface.
ms.assetid: a85f3a44-7cdf-421f-a1e4-c67a9dd0c54d
keywords:
- RPC_IF_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4652fbd08c583ad0a33638e52face9569e6ff701cb6dc2b775c7060134b60437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926438"
---
# <a name="rpc_if_handle"></a>\_handle RPC if \_

Le type de données **RPC \_ if \_ handle** déclare un handle d’interface.


```C++
typedef void __RPC_FAR* RPC_IF_HANDLE;
```



## <a name="remarks"></a>Remarques

La bibliothèque Runtime RPC utilise des descripteurs d’interface pour accéder à la structure de données de spécification d’interface. Le compilateur MIDL crée automatiquement une structure de données de spécification d’interface à partir de chaque fichier IDL et crée une variable globale de type RPC \_ si \_ handle pour la spécification de l’interface.

Le compilateur MIDL comprend un handle d’interface dans chaque fichier d’en-tête généré pour l’interface. Les fonctions qui requièrent la spécification de l’interface en tant que paramètre affichent un type de données **RPC \_ si \_ handle**. Le nom du descripteur de l’interface est le suivant :

-   *If-Name* \_ ClientIfHandle (pour le client)
-   *If-Name* \_ ServerIfHandle (pour le serveur)

La partie *If-Name* spécifie l’identificateur d’interface dans le fichier IDL.

Par exemple :

Hello \_ ClientIfHandle

Hello \_ ServerIfHandle

> [!Note]  
> La longueur maximale du nom de handle de l’interface est de 31 caractères.

 

Étant donné que les \_ parties « ClientIfHandle » et « \_ ServerIfHandle » des noms nécessitent 15 caractères, l’élément *If-Name* ne peut pas comporter plus de 16 caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h (inclure RPC. h)</dt> </dl> |



 

 





