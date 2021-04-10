---
description: Une application envoie le \_ message WM WININICHANGE à toutes les fenêtres de niveau supérieur après avoir apporté une modification au fichier WIN.INI. La fonction SystemParametersInfo envoie ce message après qu’une application a utilisé la fonction pour modifier un paramètre dans WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Message WM_WININICHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951141"
---
# <a name="wm_wininichange-message"></a>\_Message WM WININICHANGE

Une application envoie le message **WM \_ WININICHANGE** à toutes les fenêtres de niveau supérieur après avoir apporté une modification au fichier WIN.INI. La fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envoie ce message après qu’une application a utilisé la fonction pour modifier un paramètre dans WIN.INI.

> [!Note]  
> Le message **WM \_ WININICHANGE** est fourni uniquement à des fins de compatibilité avec les versions antérieures du système. Les applications doivent utiliser le message [**WM \_ SETTINGCHANGE**](wm-settingchange.md) .

 

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne contenant le nom du paramètre système qui a été modifié. Par exemple, cette chaîne peut être le nom d’une clé de registre ou le nom d’une section dans le fichier Win.ini. Ce paramètre n’est pas particulièrement utile pour déterminer quel paramètre système a changé. Par exemple, lorsque la chaîne est un nom de Registre, elle indique généralement uniquement le nœud terminal dans le registre, et non le chemin d’accès complet. De plus, certaines applications envoient ce message avec *lParam* défini sur **null**. En général, lorsque vous recevez ce message, vous devez vérifier et recharger les paramètres système qui sont utilisés par votre application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si vous traitez ce message, retournez zéro.

## <a name="remarks"></a>Notes

Pour envoyer le **message \_ WM WININICHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec le paramètre *HWND* défini **sur \_ Broadcast HWND**.

Les appels aux fonctions qui modifient WIN.INI peuvent être mappés au registre à la place. Ce mappage se produit lorsque WIN.INI et que la section en cours de modification sont spécifiées dans le Registre sous la clé suivante :

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

La modification de l’emplacement de stockage n’a aucun effet sur le comportement de ce message.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
