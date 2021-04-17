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
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483121"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence**](tag.md)
</dt> </dl>

 

 




