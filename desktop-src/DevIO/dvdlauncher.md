---
description: Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: a52ac620e5ec9aa3d9060d35921fcfd9c5bcc6e73cebf71ef336ceb54fc0806e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956908"
---
# <a name="dvdlauncher-function"></a>DvdLauncher fonction)

Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre de niveau supérieur à utiliser pour toute interface utilisateur requise.

</dd> <dt>

Lettre de *lecteur* \[ dans\]
</dt> <dd>

Lettre de lecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie et que les régions correspondent, la valeur de retour est différente de zéro. Sinon, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à StorProp.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de gestion des appareils](device-management-functions.md)
</dt> </dl>

 

