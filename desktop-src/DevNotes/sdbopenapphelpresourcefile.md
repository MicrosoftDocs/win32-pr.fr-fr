---
description: Charge le fichier de ressources AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044989"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile fonction)

Charge le fichier de ressources AppHelp.

## <a name="syntax"></a>Syntaxe


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszACResourceFile* \[ dans, facultatif\]
</dt> <dd>

Chemin d’accès au fichier de ressources. Si ce paramètre a la **valeur null**, la dll de ressource locale est ouverte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un handle au fichier de ressources ouvert.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




