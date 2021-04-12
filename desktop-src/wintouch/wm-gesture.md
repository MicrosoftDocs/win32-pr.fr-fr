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
# <a name="wm_gesture-message"></a>\_Message de mouvement WM

Transmet des informations sur un geste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Fournit des informations identifiant la commande de mouvement et les valeurs d’argument spécifiques aux mouvements. Ces informations sont les mêmes que celles passées dans le membre **ullArguments** de la structure [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) .

</dd> <dt>

*lParam* 
</dt> <dd>

Fournit un handle pour les informations identifiant la commande de mouvement et les valeurs d’argument spécifiques aux mouvements. Ces informations sont récupérées en appelant [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner 0.

Si l’application ne traite pas le message, elle doit appeler [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca). Si ce n’est pas le cas, l’application risque de provoquer une fuite de mémoire, car le handle d’entrée tactile n’est pas fermé et la mémoire de processus associée n’est pas libérée.

## <a name="remarks"></a>Notes

Le tableau suivant répertorie les commandes de mouvement prises en charge.



| ID de mouvement            | Valeur (*dwId*) | Description                                                                                                                                                                                                                                                                          |
|-----------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **début de GID \_**        | 1              | Indique qu’un mouvement générique commence.                                                                                                                                                                                                                                            |
| **\_terminaison GID**          | 2              | Indique une fin de mouvement générique.                                                                                                                                                                                                                                                     |
| **\_Zoom GID**         | 3              | Indique le début du zoom, le déplacement du zoom ou l’arrêt du zoom. Le premier message de commande de **\_ Zoom GID** commence un zoom, mais n’effectue pas de zoom. La deuxième commande de **\_ Zoom GID** déclenche un zoom par rapport à l’État contenu dans le **premier \_ Zoom GID**.                                    |
| **\_panoramique GID**          | 4              | Indique un déplacement panoramique ou un démarrage panoramique. La première commande de **\_ panoramique GID** indique un démarrage panoramique, mais n’effectue pas de panoramique. Avec le deuxième message de commande de **\_ panoramique GID** , l’application commence à effectuer le panoramique.                                                                            |
| **interversion \_ de GID**       | 5              | Indique le début de la rotation du déplacement ou de la rotation. Le premier message de commande de **\_ rotation GID** indique un mouvement de rotation de déplacement ou de rotation, mais ne pivote pas. Le deuxième message de commande de rotation **GID \_** déclenche une opération de rotation relative à l’État contenu dans le premier **GID \_**. |
| **GID \_ TWOFINGERTAP** | 6              | Indique un mouvement TAP à deux doigts.                                                                                                                                                                                                                                                    |
| **GID \_ PRESSANDTAP**  | 7              | Indique le mouvement d’appui et de pression.                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Pour activer la prise en charge héritée, les messages avec les commandes de mouvement de **\_ fin** de **GID de \_ début** et gid doivent être transférés à l’aide de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

 

Le tableau suivant indique les arguments de mouvement passés dans les paramètres *lParam* et *wParam* .



| ID de mouvement            | Mouvement        | *ullArgument*                                                                                                                                                                                                                                                                                                                                                                                            | *ptsLocation* dans la structure [**GestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)                                                  |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| **\_Zoom GID**         | Zoom avant/arrière    | Indique la distance entre les deux points.                                                                                                                                                                                                                                                                                                                                                           | Indique le centre du zoom.                                                                                 |
| **\_panoramique GID**          | Panoramique            | Indique la distance entre les deux points.                                                                                                                                                                                                                                                                                                                                                           | Indique la position actuelle du panoramique.                                                                        |
| **interversion \_ de GID**       | Pivoter (tableau croisé dynamique) | Indique l’angle de rotation si l’indicateur de **\_ début GF** est défini. Dans le cas contraire, il s’agit de la modification d’angle depuis le début de la rotation. Cela est signé pour indiquer la direction de la rotation. Utilisez les macros d’angle [**\_ de rotation GID \_ de l' \_ \_ argument**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_from_argument) et du [**GID \_ pour faire pivoter l' \_ angle \_ sur \_**](/windows/desktop/api/winuser/nf-winuser-gid_rotate_angle_to_argument) les macros d’argument pour récupérer et définir la valeur d’angle. | Cela indique le centre de la rotation qui est le point fixe autour duquel l’objet cible est pivoté. |
| **GID \_ TWOFINGERTAP** | Robinet à deux doigts | Indique la distance entre les deux doigts.                                                                                                                                                                                                                                                                                                                                                          | Indique le Centre des deux doigts.                                                                          |
| **GID \_ PRESSANDTAP**  | Appuyez et appuyez sur  | Indique le delta entre le premier doigt et le deuxième doigt. Cette valeur est stockée dans les 32 bits inférieurs du *ullArgument* dans une structure de **points** .                                                                                                                                                                                                                                             | Indique la position de la première partie du doigt.                                                       |



 

> [!Note]  
> Toutes les distances et positions sont fournies en coordonnées d’écran physiques.

 

> [!Note]  
> Les paramètres *dwId* et *ullArgument* ne doivent être pris en compte que pour accompagner les \_ \* commandes GID et ne doivent pas être modifiés par les applications.

 

## <a name="examples"></a>Exemples

Le code suivant montre comment obtenir des informations spécifiques au geste associées à ce message.

> [!Note]  
> Vous devez toujours transférer les messages non gérés à [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) et vous devez fermer le handle d’entrée de mouvement pour les messages que vous gérez avec un appel à [**CloseGestureInfoHandle**](/windows/desktop/api/winuser/nf-winuser-closegestureinfohandle). Dans cet exemple, le comportement du gestionnaire de mouvements par défaut sera supprimé, car le handle TOUCHINPUT est fermé dans chacun des cas de mouvement. Si vous avez supprimé les cas dans le code ci-dessus pour les messages non gérés, le gestionnaire de mouvements par défaut traite les messages en les transférant vers [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) dans le cas par défaut.

 


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Notifications](notifications.md)
</dt> <dt>

[Guide de programmation des gestes tactiles Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

