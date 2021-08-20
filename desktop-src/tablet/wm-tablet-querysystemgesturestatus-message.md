---
description: Envoyé lorsque le système demande à une fenêtre les gestes système qu’il souhaite recevoir.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Message WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbde7fb6147771cadcac8dba4d6fc104432d6c6793a9e72238d99b4b64b5065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041701"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a>\_Message QUERYSYSTEMGESTURESTATUS de tablette WM \_

Envoyé lorsque le système demande à une fenêtre les gestes système qu’il souhaite recevoir.


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de point qui représente les coordonnées d’écran.

</dd> </dl>

## <a name="remarks"></a>Remarques

En gérant ce message, vous pouvez désactiver dynamiquement les raccourcis pour les régions d’une fenêtre.

> [!Note]  
> Le *lParam* peut être converti en coordonnées x et y à l’aide des `GET_X_LPARAM` `GET_Y_LPARAM` macros et.

 

Par défaut, votre fenêtre recevra tous les événements de mouvement système. Vous pouvez choisir les événements que vous souhaitez que votre fenêtre reçoit et les événements que vous souhaitez désactiver en répondant au message **WM \_ \_ QUERYSYSTEMGESTURESTATUS** dans votre **WndProc**. Le **message \_ WM \_ QUERYSYSTEMGESTURESTATUS** est défini dans tpcshrd. h. Les valeurs permettant d’activer et de désactiver les gestes système du Tablet système sont également définies dans tpcshrd. h comme suit :

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> La désactivation de la fonction appuyer et maintenir permet d’améliorer la réactivité des clics de souris, car cette fonctionnalité crée un délai d’attente pour faire la distinction entre les deux opérations.

 

Soyez prudent lors du traitement du message **WM \_ \_ QUERYSYSTEMGESTURESTATUS** . **WM \_ La \_ QUERYSYSTEMGESTURESTATUS de tablette** est transmise à l’aide de la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Si vous appelez des méthodes sur une interface COM, cet objet doit être dans le même processus. Si ce n’est pas le cas, COM lève une exception.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment désactiver les raccourcis pour une région à l’aide de WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



L’exemple suivant montre comment désactiver différentes fonctionnalités de raccourcis pour une fenêtre entière.


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
