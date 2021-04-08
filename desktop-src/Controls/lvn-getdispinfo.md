---
title: LVN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View à sa fenêtre parente. Il s’agit d’une demande de la fenêtre parente pour fournir les informations nécessaires à l’affichage ou au tri d’un élément de liste. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Contrôles Windows de code de notification LVN_GETDISPINFO
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744004"
---
# <a name="lvn_getdispinfo-notification-code"></a>\_Code de notification LVN GETDISPINFO

Envoyé par un contrôle List-View à sa fenêtre parente. Il s’agit d’une demande de la fenêtre parente pour fournir les informations nécessaires à l’affichage ou au tri d’un élément de liste. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . En entrée, la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenue dans cette structure spécifie le type d’informations requis et identifie l’élément ou le sous-élément d’intérêt. Utilisez la structure **LVITEM** pour retourner les informations demandées au contrôle. Si votre gestionnaire de messages définit l' \_ indicateur LVIF di \_ SETITEM dans le membre **Mask** de la structure **LVITEM** , le contrôle List-View stocke les informations demandées et ne le redemande pas.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Le paramètre *wParam* contient le code de notification.

Un contrôle List-View envoie le code de notification **LVN \_ GETDISPINFO** pour récupérer des informations d’élément stockées par l’application plutôt que par le contrôle. Les informations peuvent être du texte ou des icônes pour un élément. Il peut également s’agir d’informations sur l’état de l’élément. Consultez le [**message \_ SETCALLBACKMASK LVM**](lvm-setcallbackmask.md) pour plus d’informations sur l’implémentation de l’état des éléments sur la base d’un rappel.

Pour plus d’informations sur les rappels de vue de liste, consultez [éléments de rappel et masque de rappel](list-view-controls-overview.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment ce code de notification peut être géré pour définir le texte dans les colonnes d’un affichage de liste. Les données de chaque élément sont stockées dans la structure suivante.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



Les éléments suivants proviennent du \_ Gestionnaire de notification WM dans la procédure de dialogue.


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ GETDISPINFOW** (Unicode) et **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





