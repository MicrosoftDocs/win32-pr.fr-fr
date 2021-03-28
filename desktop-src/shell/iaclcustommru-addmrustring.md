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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991541"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



 

 




