---
description: La fonction IsWindowRedirectedForPrint détermine si la fenêtre spécifiée est actuellement redirigée pour l’impression.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519481"
---
# <a name="iswindowredirectedforprint-function"></a>IsWindowRedirectedForPrint fonction)

La fonction **IsWindowRedirectedForPrint** détermine si la fenêtre spécifiée est actuellement redirigée pour l’impression.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fenêtre est actuellement redirigée pour impression, la fonction retourne une valeur différente de zéro ; Sinon, elle retourne zéro.

## <a name="remarks"></a>Notes

Une fenêtre est redirigée pour impression quand elle traite un appel à [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow). Dans un appel à **PrintWindow**, une fenêtre affiche son contenu dans un contexte de périphérique hors écran.

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**\_impression WM**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**\_PRINTCLIENT WM**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

