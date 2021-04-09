---
description: Envoyé lorsque le système demande à une fenêtre les gestes système qu’il souhaite recevoir.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Message WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862485"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="bfac6-103">\_Message QUERYSYSTEMGESTURESTATUS de tablette WM \_</span><span class="sxs-lookup"><span data-stu-id="bfac6-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="bfac6-104">Envoyé lorsque le système demande à une fenêtre les gestes système qu’il souhaite recevoir.</span><span class="sxs-lookup"><span data-stu-id="bfac6-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="bfac6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfac6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfac6-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bfac6-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfac6-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="bfac6-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bfac6-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfac6-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfac6-109">Valeur de point qui représente les coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="bfac6-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfac6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bfac6-110">Remarks</span></span>

<span data-ttu-id="bfac6-111">En gérant ce message, vous pouvez désactiver dynamiquement les raccourcis pour les régions d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bfac6-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="bfac6-112">Le *lParam* peut être converti en coordonnées x et y à l’aide des `GET_X_LPARAM` `GET_Y_LPARAM` macros et.</span><span class="sxs-lookup"><span data-stu-id="bfac6-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="bfac6-113">Par défaut, votre fenêtre recevra tous les événements de mouvement système.</span><span class="sxs-lookup"><span data-stu-id="bfac6-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="bfac6-114">Vous pouvez choisir les événements que vous souhaitez que votre fenêtre reçoit et les événements que vous souhaitez désactiver en répondant au message **WM \_ \_ QUERYSYSTEMGESTURESTATUS** dans votre **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="bfac6-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="bfac6-115">Le **message \_ WM \_ QUERYSYSTEMGESTURESTATUS** est défini dans tpcshrd. h.</span><span class="sxs-lookup"><span data-stu-id="bfac6-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="bfac6-116">Les valeurs permettant d’activer et de désactiver les gestes système du Tablet système sont également définies dans tpcshrd. h comme suit :</span><span class="sxs-lookup"><span data-stu-id="bfac6-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

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
> <span data-ttu-id="bfac6-117">La désactivation de la fonction appuyer et maintenir permet d’améliorer la réactivité des clics de souris, car cette fonctionnalité crée un délai d’attente pour faire la distinction entre les deux opérations.</span><span class="sxs-lookup"><span data-stu-id="bfac6-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="bfac6-118">Soyez prudent lors du traitement du message **WM \_ \_ QUERYSYSTEMGESTURESTATUS** .</span><span class="sxs-lookup"><span data-stu-id="bfac6-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="bfac6-119">**WM \_ La \_ QUERYSYSTEMGESTURESTATUS de tablette** est transmise à l’aide de la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="bfac6-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="bfac6-120">Si vous appelez des méthodes sur une interface COM, cet objet doit être dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="bfac6-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="bfac6-121">Si ce n’est pas le cas, COM lève une exception.</span><span class="sxs-lookup"><span data-stu-id="bfac6-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="bfac6-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="bfac6-122">Examples</span></span>

<span data-ttu-id="bfac6-123">L’exemple suivant montre comment désactiver les raccourcis pour une région à l’aide de WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.</span><span class="sxs-lookup"><span data-stu-id="bfac6-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


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



<span data-ttu-id="bfac6-124">L’exemple suivant montre comment désactiver différentes fonctionnalités de raccourcis pour une fenêtre entière.</span><span class="sxs-lookup"><span data-stu-id="bfac6-124">The following example shows how to disable various flicks features for an entire window.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bfac6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfac6-125">Requirements</span></span>



| <span data-ttu-id="bfac6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfac6-126">Requirement</span></span> | <span data-ttu-id="bfac6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfac6-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfac6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfac6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bfac6-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfac6-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfac6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfac6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bfac6-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfac6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfac6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfac6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfac6-133"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfac6-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
