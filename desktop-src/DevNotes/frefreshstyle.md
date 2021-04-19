---
description: Recharge les paramètres de couleur à partir du Registre.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: FRefreshStyle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545458"
---
# <a name="frefreshstyle-function"></a>FRefreshStyle fonction)

Recharge les paramètres de couleur à partir du Registre.

## <a name="syntax"></a>Syntaxe


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur TRUE en cas de réussite ; Sinon, FALSe.

## <a name="remarks"></a>Notes

Cette fonction n’est pas associée à une bibliothèque d’importation ou un fichier d’en-tête ; elle doit être appelée à l’aide des fonctions [**LoadLibrary**](-loadlibrary.md) et [**GetProcAddress**](-getprocaddress-.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetProcAddress**](-getprocaddress-.md)
</dt> <dt>

[**LoadLibrary**](-loadlibrary.md)
</dt> </dl>

 

 




