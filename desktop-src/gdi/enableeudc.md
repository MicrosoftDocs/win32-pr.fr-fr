---
description: Cette fonction active ou désactive la prise en charge des caractères définis par l’utilisateur final (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972687"
---
# <a name="enableeudc-function"></a>EnableEUDC fonction)

Cette fonction active ou désactive la prise en charge des caractères définis par l’utilisateur final (EUDC).

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fEnableEUDC* \[ dans\]
</dt> <dd>

Valeur booléenne qui a la valeur **true** pour activer EUDC et la valeur **false** pour désactiver EUDC.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

Si EUDC est désactivé, toute tentative d’affichage des caractères EUDC entraîne des glyphes manquants ou incorrects.

Pendant la session multisession, cette fonction affecte uniquement la session active.

Il est recommandé d’utiliser cette fonction avec Windows XP SP2 ou version ultérieure.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Bibliothèque<br/>                  | <dl> <dt>GDI32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



 

 




