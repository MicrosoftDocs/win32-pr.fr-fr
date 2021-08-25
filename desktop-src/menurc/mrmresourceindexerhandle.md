---
title: MrmResourceIndexerHandle, structure (MrmResourceIndexer. h)
description: Représente un handle opaque d’un objet indexeur de ressource. Le handle est géré par le système d’exploitation. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: E3ED8AB8-39B8-419C-9570-1CC6B2CFE8D0
keywords:
- Menus de la structure MrmResourceIndexerHandle et autres ressources
- Menus du pointeur de structure PMrmResourceIndexerHandle et autres ressources
topic_type:
- apiref
api_name:
- MrmResourceIndexerHandle
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c9cd18d6c828d5f9b5187f866d8ab637dfd4d58c3da0a8569bd8c910c7e872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825689"
---
# <a name="mrmresourceindexerhandle-structure"></a>MrmResourceIndexerHandle, structure

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Représente un handle opaque d’un objet indexeur de ressource. Le handle est géré par le système d’exploitation. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MrmResourceIndexerHandle {
  PVOID handle;
} MrmResourceIndexerHandle, *PMrmResourceIndexerHandle;
```



## <a name="members"></a>Membres

<dl> <dt>

**traitée**
</dt> <dd>

Type : **pVoid**

</dd> <dd>

Handle opaque vers un objet indexeur de ressource.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows \[Applications de bureau serveur uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

