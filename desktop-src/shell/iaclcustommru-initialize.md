---
description: Charge une liste de chaînes dans la liste des derniers fichiers utilisés (MRU) à partir du Registre.
title: 'IACLCustomMRU :: Initialize, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991540"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU :: Initialize, méthode

Charge une liste de chaînes dans la liste des derniers fichiers utilisés (MRU) à partir du Registre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszMRURegKey* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une mémoire tampon qui contient la clé de registre contenant les chaînes de la liste MRU.

</dd> <dt>

*dwMax* \[ dans\]
</dt> <dd>

Type : **DWORD**

Nombre maximal d’entrées qui peuvent être extraites de *pwszMRURegKey*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



 

 




