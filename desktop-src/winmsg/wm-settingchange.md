---
description: Message qui est envoyé à toutes les fenêtres de niveau supérieur lorsque la fonction SystemParametersInfo modifie un paramètre à l’échelle du système ou lorsque les paramètres de stratégie ont été modifiés.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Message WM_SETTINGCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302f156da905263ed7f3d1d331d4dbb25af5b3e81d9df6136281c7dbc7b3914c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710039"
---
# <a name="wm_settingchange-message"></a>\_Message WM SETTINGCHANGE

Message qui est envoyé à toutes les fenêtres de niveau supérieur lorsque la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) modifie un paramètre à l’échelle du système ou lorsque les paramètres de stratégie ont été modifiés.

Les applications doivent envoyer **WM \_ SETTINGCHANGE** à toutes les fenêtres de niveau supérieur lorsqu’elles apportent des modifications aux paramètres système. (Ce message ne peut pas être envoyé directement à une fenêtre.) Pour envoyer le **message \_ WM SETTINGCHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) avec le paramètre *HWND* défini **sur \_ Broadcast HWND**.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Lorsque le système envoie ce message à la suite d’un appel [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , le paramètre *wParam* est la valeur du paramètre *UiAction* passé à la fonction **SystemParametersInfo** . Pour obtenir la liste des valeurs, consultez **SystemParametersInfo**.

Lorsque le système envoie ce message suite à une modification des paramètres de stratégie, ce paramètre indique le type de stratégie qui a été appliqué. Cette valeur est 1 si la stratégie de l’ordinateur a été appliquée ou zéro si la stratégie de l’utilisateur a été appliquée.

Lorsque le système envoie ce message suite à une modification des paramètres régionaux, ce paramètre est égal à zéro.

Quand une application envoie ce message, ce paramètre doit avoir la **valeur null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quand le système envoie ce message à la suite d’un appel [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* est un pointeur vers une chaîne qui indique la zone contenant le paramètre système qui a été modifié. Ce paramètre n’indique généralement pas le paramètre système spécifique modifié. (Notez que certaines applications envoient ce message avec *lParam* défini sur **null**.) En général, lorsque vous recevez ce message, vous devez vérifier et recharger les paramètres système qui sont utilisés par votre application.

Cette chaîne peut être le nom d’une clé de registre ou le nom d’une section dans le fichier Win.ini. Lorsque la chaîne est un nom de Registre, elle indique généralement uniquement le nœud terminal dans le registre, et non le chemin d’accès complet.

Lorsque le système envoie ce message suite à une modification des paramètres de stratégie, ce paramètre pointe vers la chaîne « stratégie ».

Lorsque le système envoie ce message suite à une modification des paramètres régionaux, ce paramètre pointe vers la chaîne « Intl ».

Pour appliquer une modification dans les variables d’environnement du système ou de l’utilisateur, diffusez ce message avec *lParam* défini sur la chaîne « environnement ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si vous traitez ce message, retournez zéro.

## <a name="remarks"></a>Remarques

Le paramètre *lParam* indique quelle mesure système a changé, par exemple « ConvertibleSlateMode » si l’indicateur ConvertibleSlateMode a été activé ou « SystemDockMode » si l’indicateur ancré a été activé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de stratégie](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
