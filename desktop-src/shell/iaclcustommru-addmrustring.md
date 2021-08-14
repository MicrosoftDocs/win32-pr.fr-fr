---
description: Ajoute une entrée à la liste des derniers fichiers utilisés (MRU).
title: 'IACLCustomMRU :: AddMRUString, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: e5acd71a56ef0dd569315ee924313b10e27e6a4ba7ca75d1dbfa0d1e50932cdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223593"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU :: AddMRUString, méthode

Ajoute une entrée à la liste des derniers fichiers utilisés (MRU).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszEntry* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une mémoire tampon contenant la nouvelle entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 




