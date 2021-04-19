---
title: TVN_ASYNCDRAW le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View à son parent lorsque le dessin d’une icône ou d’une superposition a échoué. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Contrôles Windows de code de notification TVN_ASYNCDRAW
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542868"
---
# <a name="tvn_asyncdraw-notification-code"></a>\_Code de notification TVN ASYNCDRAW

Envoyé par un contrôle Tree-View à son parent lorsque le dessin d’une icône ou d’une superposition a échoué. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . La structure **NMTVASYNCDRAW** contient la raison de l’échec du dessin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le contrôle Tree-View doit avoir le style étendu [**TV \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) . Notez que cela équivaut à l’indicateur LVN ASYNCDRAWN de l’affichage \_ des listes et à son style correspondant.

Ce contrôle ne dessine pas de façon asynchrone. Le mode asynchrone est utilisé dans le contexte selon lequel le contrôle Tree-View n’extrait pas de façon synchrone une image si elle n’est pas disponible. (Par exemple, l’image peut ne pas être disponible si le contrôle d’arborescence utilise une liste d’images éparses, dans la mesure où l’image peut être déchargée.) Au lieu de cela, lorsqu’une image n’est pas disponible, le contrôle demande de manière synchrone à la parente l’action à entreprendre en lui envoyant une \_ notification ASYNCDRAW TVN avec une structure [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) . Le membre **HR** de cette structure décrit la raison de l’échec du dessin du contrôle. Un résultat **HR** de E \_ en attente signifie que l’image n’est pas présente (l’image doit être extraite). Success indique que l’image est présente mais pas à la qualité d’image requise.

Le parent définit le membre **dwRetFlags** de la structure pour informer le contrôle de la procédure à suivre. Par exemple, le parent peut retourner une autre image, dans le membre **iRetImageIndex** , pour le contrôle à dessiner. Dans ce cas, le parent définit le membre **dwRetFlags** sur adrf \_ DRAWIMAGE. Si le contrôle trouve que l’image retournée n’a pas été extraite, une autre \_ notification TVN ASYNCDRAW peut être envoyée par le contrôle.

Si une image n’est pas disponible, l’idée derrière asynchrone consiste à autoriser le parent à effectuer l’extraction en arrière-plan afin que l’extraction ne bloque pas le thread d’interface utilisateur, autrement dit, le thread sur lequel se trouve le contrôle. Le parent peut retourner ADRF \_ DRAWNOTHING au contrôle, puis lancer un thread d’arrière-plan pour extraire l’icône. Une fois extrait, le parent peut définir l’icône dans le contrôle TreeView avec la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem). Cela amène l’arborescence à invalider l’élément et à le repeindre avec l’image extraite dans la liste d’images.

L’exemple de code suivant, à utiliser dans le cadre d’un programme plus volumineux, montre comment un parent peut traiter deux codes de retour possibles dans cette notification par un contrôle et déterminer l’action que le contrôle doit prendre. La définition de **dwRetFlags** n’est pas affichée.


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





