---
title: Message WM_GESTURE (winuser. h)
description: Transmet des informations sur un geste.
ms.assetid: 4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8
keywords:
- WM_GESTURE message Windows tactile
topic_type:
- apiref
api_name:
- WM_GESTURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1184d1f54d110f84630a727decb91ad28e6c08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384939"
---
# <a name="wm_gesture-message"></a><span data-ttu-id="cb7d1-104">\_Message de mouvement WM</span><span class="sxs-lookup"><span data-stu-id="cb7d1-104">WM\_GESTURE message</span></span>

<span data-ttu-id="cb7d1-105">Transmet des informations sur un geste.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-105">Passes information about a gesture.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb7d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb7d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb7d1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7d1-108">Fournit des informations identifiant la commande de mouvement et les valeurs d’argument spécifiques aux mouvements.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-108">Provides information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="cb7d1-109">Ces informations sont les mêmes que celles passées dans le membre **ullArguments** de la structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .</span><span class="sxs-lookup"><span data-stu-id="cb7d1-109">This information is the same information passed in the **ullArguments** member of the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cb7d1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb7d1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb7d1-111">Fournit un handle pour les informations identifiant la commande de mouvement et les valeurs d’argument spécifiques aux mouvements.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-111">Provides a handle to information identifying the gesture command and gesture-specific argument values.</span></span> <span data-ttu-id="cb7d1-112">Ces informations sont récupérées en appelant [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span><span class="sxs-lookup"><span data-stu-id="cb7d1-112">This information is retrieved by calling [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7d1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cb7d1-113">Return value</span></span>

<span data-ttu-id="cb7d1-114">Si une application traite ce message, elle doit retourner 0.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-114">If an application processes this message, it should return 0.</span></span>

<span data-ttu-id="cb7d1-115">Si l’application ne traite pas le message, elle doit appeler [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="cb7d1-115">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="cb7d1-116">Si ce n’est pas le cas, l’application risque de provoquer une fuite de mémoire, car le handle d’entrée tactile n’est pas fermé et la mémoire de processus associée n’est pas libérée.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-116">Not doing so will cause the application to leak memory because the touch input handle will not be closed and associated process memory will not be freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb7d1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cb7d1-117">Remarks</span></span>

<span data-ttu-id="cb7d1-118">Le tableau suivant répertorie les commandes de mouvement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-118">The following table lists the supported gesture commands.</span></span>



| <span data-ttu-id="cb7d1-119">ID de mouvement</span><span class="sxs-lookup"><span data-stu-id="cb7d1-119">Gesture ID</span></span>            | <span data-ttu-id="cb7d1-120">Valeur (*dwId*)</span><span class="sxs-lookup"><span data-stu-id="cb7d1-120">Value (*dwID*)</span></span> | <span data-ttu-id="cb7d1-121">Description</span><span class="sxs-lookup"><span data-stu-id="cb7d1-121">Description</span></span>                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7d1-122">**début de GID \_**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-122">**GID\_BEGIN**</span></span>        | <span data-ttu-id="cb7d1-123">1</span><span class="sxs-lookup"><span data-stu-id="cb7d1-123">1</span></span>              | <span data-ttu-id="cb7d1-124">Indique qu’un mouvement générique commence.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-124">Indicates a generic gesture is beginning.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="cb7d1-125">**\_terminaison GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-125">**GID\_END**</span></span>          | <span data-ttu-id="cb7d1-126">2</span><span class="sxs-lookup"><span data-stu-id="cb7d1-126">2</span></span>              | <span data-ttu-id="cb7d1-127">Indique une fin de mouvement générique.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-127">Indicates a generic gesture end.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cb7d1-128">**\_Zoom GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-128">**GID\_ZOOM**</span></span>         | <span data-ttu-id="cb7d1-129">3</span><span class="sxs-lookup"><span data-stu-id="cb7d1-129">3</span></span>              | <span data-ttu-id="cb7d1-130">Indique le début du zoom, le déplacement du zoom ou l’arrêt du zoom.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-130">Indicates zoom start, zoom move, or zoom stop.</span></span> <span data-ttu-id="cb7d1-131">Le premier message de commande de **\_ Zoom GID** commence un zoom, mais n’effectue pas de zoom.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-131">The first **GID\_ZOOM** command message begins a zoom but does not cause any zooming.</span></span> <span data-ttu-id="cb7d1-132">La deuxième commande de **\_ Zoom GID** déclenche un zoom par rapport à l’État contenu dans le **premier \_ Zoom GID**.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-132">The second **GID\_ZOOM** command triggers a zoom relative to the state contained in the first **GID\_ZOOM**.</span></span>                                    |
| <span data-ttu-id="cb7d1-133">**\_panoramique GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-133">**GID\_PAN**</span></span>          | <span data-ttu-id="cb7d1-134">4</span><span class="sxs-lookup"><span data-stu-id="cb7d1-134">4</span></span>              | <span data-ttu-id="cb7d1-135">Indique un déplacement panoramique ou un démarrage panoramique.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-135">Indicates pan move or pan start.</span></span> <span data-ttu-id="cb7d1-136">La première commande de **\_ panoramique GID** indique un démarrage panoramique, mais n’effectue pas de panoramique.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-136">The first **GID\_PAN** command indicates a pan start but does not perform any panning.</span></span> <span data-ttu-id="cb7d1-137">Avec le deuxième message de commande de **\_ panoramique GID** , l’application commence à effectuer le panoramique.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-137">With the second **GID\_PAN** command message, the application will begin panning.</span></span>                                                                            |
| <span data-ttu-id="cb7d1-138">**interversion \_ de GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-138">**GID\_ROTATE**</span></span>       | <span data-ttu-id="cb7d1-139">5</span><span class="sxs-lookup"><span data-stu-id="cb7d1-139">5</span></span>              | <span data-ttu-id="cb7d1-140">Indique le début de la rotation du déplacement ou de la rotation.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-140">Indicates rotate move or rotate start.</span></span> <span data-ttu-id="cb7d1-141">Le premier message de commande de **\_ rotation GID** indique un mouvement de rotation de déplacement ou de rotation, mais ne pivote pas.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-141">The first **GID\_ROTATE** command message indicates a rotate move or rotate start but will not rotate.</span></span> <span data-ttu-id="cb7d1-142">Le deuxième message de commande de rotation **GID \_** déclenche une opération de rotation relative à l’État contenu dans le premier **GID \_**.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-142">The second **GID\_ROTATE** command message will trigger a rotation operation relative to state contained in the first **GID\_ROTATE**.</span></span> |
| <span data-ttu-id="cb7d1-143">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-143">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="cb7d1-144">6</span><span class="sxs-lookup"><span data-stu-id="cb7d1-144">6</span></span>              | <span data-ttu-id="cb7d1-145">Indique un mouvement TAP à deux doigts.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-145">Indicates two-finger tap gesture.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cb7d1-146">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-146">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="cb7d1-147">7</span><span class="sxs-lookup"><span data-stu-id="cb7d1-147">7</span></span>              | <span data-ttu-id="cb7d1-148">Indique le mouvement d’appui et de pression.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-148">Indicates the press and tap gesture.</span></span>                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="cb7d1-149">Pour activer la prise en charge héritée, les messages avec les commandes de mouvement de **\_ fin** de **GID de \_ début** et gid doivent être transférés à l’aide de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="cb7d1-149">In order to enable legacy support, messages with the **GID\_BEGIN** and **GID\_END** gesture commands need to be forwarded using [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

 

<span data-ttu-id="cb7d1-150">Le tableau suivant indique les arguments de mouvement passés dans les paramètres *lParam* et *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cb7d1-150">The following table indicates the gesture arguments passed in the *lParam* and *wParam* parameters.</span></span>



| <span data-ttu-id="cb7d1-151">ID de mouvement</span><span class="sxs-lookup"><span data-stu-id="cb7d1-151">Gesture ID</span></span>            | <span data-ttu-id="cb7d1-152">Mouvement</span><span class="sxs-lookup"><span data-stu-id="cb7d1-152">Gesture</span></span>        | <span data-ttu-id="cb7d1-153">*ullArgument*</span><span class="sxs-lookup"><span data-stu-id="cb7d1-153">*ullArgument*</span></span>                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="cb7d1-154">*ptsLocation* dans la structure [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)</span><span class="sxs-lookup"><span data-stu-id="cb7d1-154">*ptsLocation* in [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) structure</span></span>                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7d1-155">**\_Zoom GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-155">**GID\_ZOOM**</span></span>         | <span data-ttu-id="cb7d1-156">Zoom avant/arrière</span><span class="sxs-lookup"><span data-stu-id="cb7d1-156">Zoom In/Out</span></span>    | <span data-ttu-id="cb7d1-157">Indique la distance entre les deux points.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-157">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="cb7d1-158">Indique le centre du zoom.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-158">Indicates the center of the zoom.</span></span>                                                                                 |
| <span data-ttu-id="cb7d1-159">**\_panoramique GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-159">**GID\_PAN**</span></span>          | <span data-ttu-id="cb7d1-160">Panoramique</span><span class="sxs-lookup"><span data-stu-id="cb7d1-160">Pan</span></span>            | <span data-ttu-id="cb7d1-161">Indique la distance entre les deux points.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-161">Indicates the distance between the two points.</span></span>                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="cb7d1-162">Indique la position actuelle du panoramique.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-162">Indicates the current position of the pan.</span></span>                                                                        |
| <span data-ttu-id="cb7d1-163">**interversion \_ de GID**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-163">**GID\_ROTATE**</span></span>       | <span data-ttu-id="cb7d1-164">Pivoter (tableau croisé dynamique)</span><span class="sxs-lookup"><span data-stu-id="cb7d1-164">Rotate (pivot)</span></span> | <span data-ttu-id="cb7d1-165">Indique l’angle de rotation si l’indicateur de **\_ début GF** est défini.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-165">Indicates the angle of rotation if the **GF\_BEGIN** flag is set.</span></span> <span data-ttu-id="cb7d1-166">Dans le cas contraire, il s’agit de la modification d’angle depuis le début de la rotation.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-166">Otherwise, this is the angle change since the rotation has started.</span></span> <span data-ttu-id="cb7d1-167">Cela est signé pour indiquer la direction de la rotation.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-167">This is signed to indicate the direction of the rotation.</span></span> <span data-ttu-id="cb7d1-168">Utilisez les macros d’angle [**\_ de rotation GID \_ de l' \_ \_ argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) et du [**GID \_ pour faire pivoter l' \_ angle \_ sur \_**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) les macros d’argument pour récupérer et définir la valeur d’angle.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-168">Use the [**GID\_ROTATE\_ANGLE\_FROM\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) and [**GID\_ROTATE\_ANGLE\_TO\_ARGUMENT**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) macros to get and set the angle value.</span></span> | <span data-ttu-id="cb7d1-169">Cela indique le centre de la rotation qui est le point fixe autour duquel l’objet cible est pivoté.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-169">This indicates the center of the rotation which is the stationary point that the target object is rotated around.</span></span> |
| <span data-ttu-id="cb7d1-170">**GID \_ TWOFINGERTAP**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-170">**GID\_TWOFINGERTAP**</span></span> | <span data-ttu-id="cb7d1-171">Robinet à deux doigts</span><span class="sxs-lookup"><span data-stu-id="cb7d1-171">Two-finger Tap</span></span> | <span data-ttu-id="cb7d1-172">Indique la distance entre les deux doigts.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-172">Indicates the distance between the two fingers.</span></span>                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="cb7d1-173">Indique le Centre des deux doigts.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-173">Indicates the center of the two fingers.</span></span>                                                                          |
| <span data-ttu-id="cb7d1-174">**GID \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="cb7d1-174">**GID\_PRESSANDTAP**</span></span>  | <span data-ttu-id="cb7d1-175">Appuyez et appuyez sur</span><span class="sxs-lookup"><span data-stu-id="cb7d1-175">Press and Tap</span></span>  | <span data-ttu-id="cb7d1-176">Indique le delta entre le premier doigt et le deuxième doigt.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-176">Indicates the delta between the first finger and the second finger.</span></span> <span data-ttu-id="cb7d1-177">Cette valeur est stockée dans les 32 bits inférieurs du *ullArgument* dans une structure de **points** .</span><span class="sxs-lookup"><span data-stu-id="cb7d1-177">This value is stored in the lower 32 bits of the *ullArgument* in a **POINT** structure.</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="cb7d1-178">Indique la position de la première partie du doigt.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-178">Indicates the position that the first finger comes down on.</span></span>                                                       |



 

> [!Note]  
> <span data-ttu-id="cb7d1-179">Toutes les distances et positions sont fournies en coordonnées d’écran physiques.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-179">All distances and positions are provided in physical screen coordinates.</span></span>

 

> [!Note]  
> <span data-ttu-id="cb7d1-180">Les paramètres *dwId* et *ullArgument* ne doivent être pris en compte que pour accompagner les \_ \* commandes GID et ne doivent pas être modifiés par les applications.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-180">The *dwID* and *ullArgument* parameters should only be considered to be accompanying the GID\_\* commands and should not be altered by applications.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cb7d1-181">Exemples</span><span class="sxs-lookup"><span data-stu-id="cb7d1-181">Examples</span></span>

<span data-ttu-id="cb7d1-182">Le code suivant montre comment obtenir des informations spécifiques au geste associées à ce message.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-182">The following code illustrates how to obtain gesture-specific information associated with this message.</span></span>

> [!Note]  
> <span data-ttu-id="cb7d1-183">Vous devez toujours transférer les messages non gérés à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) et vous devez fermer le handle d’entrée de mouvement pour les messages que vous gérez avec un appel à [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span><span class="sxs-lookup"><span data-stu-id="cb7d1-183">You should always forward unhandled messages to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) and should close the gesture input handle for messages that you do handle with a call to [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle).</span></span> <span data-ttu-id="cb7d1-184">Dans cet exemple, le comportement du gestionnaire de mouvements par défaut sera supprimé, car le handle TOUCHINPUT est fermé dans chacun des cas de mouvement.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-184">In this example, the default gesture handler behavior will be suppressed because the TOUCHINPUT handle is closed in each of the gesture cases.</span></span> <span data-ttu-id="cb7d1-185">Si vous avez supprimé les cas dans le code ci-dessus pour les messages non gérés, le gestionnaire de mouvements par défaut traite les messages en les transférant vers [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) dans le cas par défaut.</span><span class="sxs-lookup"><span data-stu-id="cb7d1-185">If you removed the cases in the above code for unhandled messages, the default gesture handler would process the messages by getting forwarded to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) in the default case.</span></span>

 


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="requirements"></a><span data-ttu-id="cb7d1-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb7d1-186">Requirements</span></span>



| <span data-ttu-id="cb7d1-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb7d1-187">Requirement</span></span> | <span data-ttu-id="cb7d1-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb7d1-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7d1-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7d1-189">Minimum supported client</span></span><br/> | <span data-ttu-id="cb7d1-190">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb7d1-190">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="cb7d1-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb7d1-191">Minimum supported server</span></span><br/> | <span data-ttu-id="cb7d1-192">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb7d1-192">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="cb7d1-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb7d1-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb7d1-194"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb7d1-194"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7d1-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb7d1-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7d1-196">Notifications</span><span class="sxs-lookup"><span data-stu-id="cb7d1-196">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="cb7d1-197">Guide de programmation des gestes tactiles Windows</span><span class="sxs-lookup"><span data-stu-id="cb7d1-197">Windows Touch Gestures Programming Guide</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

