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
ms.openlocfilehash: 5c071d76712877650bba8ecf502687538bb6ac354e62a0285dc08e2f22f25873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103689"
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

## <a name="remarks"></a>Remarques

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

 

 




