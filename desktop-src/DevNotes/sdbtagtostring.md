---
description: Récupère le nom complet de la BALIse spécifiée.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 22ddb526e332b335e88ecc7aaa770615220f6b0dde838386093e2813fe964e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044839"
---
# <a name="sdbtagtostring-function"></a>SdbTagToString fonction)

Récupère le nom complet de la BALIse spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*balise* \[ dans\]
</dt> <dd>

BALIse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne un pointeur vers la chaîne se terminant par null ou « InvalidTag ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence**](tag.md)
</dt> </dl>

 

 




