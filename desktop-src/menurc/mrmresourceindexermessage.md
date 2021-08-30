---
title: MrmResourceIndexerMessage, structure (MrmResourceIndexer. h)
description: Représente un message généré par un indexeur de ressource. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Menus de la structure MrmResourceIndexerMessage et autres ressources
- Menus du pointeur de structure PMrmResourceIndexerMessage et autres ressources
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54751d11816a121ca9a7678a431219f6c12a8bf103c314420f739948d97e8f38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939769"
---
# <a name="mrmresourceindexermessage-structure"></a>MrmResourceIndexerMessage, structure

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Représente un message généré par un indexeur de ressource. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Membres

<dl> <dt>

**severity**
</dt> <dd>

Type : **[ **MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Valeur indiquant la gravité du message.

</dd> <dt>

**id**
</dt> <dd>

Type : **ULong**

</dd> <dd>

Identificateur unique du message.

</dd> <dt>

**text**
</dt> <dd>

Type : **PCWSTR**

</dd> <dd>

Texte du message. Ne libérez pas ce pointeur. la mémoire est détenue par le système d’exploitation.

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

 

