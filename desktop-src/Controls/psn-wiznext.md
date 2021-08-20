---
title: PSN_WIZNEXT le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton suivant dans un Assistant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dead2de1e21631b2b8e13cb54e3ee45d5d3bc29f2234380c31ec134c3790eae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169629"
---
# <a name="psn_wiznext-notification-code"></a>\_Code de notification PSN WIZNEXT

Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **suivant** dans un Assistant. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification. Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés. Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 pour permettre à l’Assistant de passer à la page suivante. Retourne-1 pour empêcher l’Assistant de modifier les pages. Pour afficher une page particulière, retournez son identificateur de ressource de boîte de dialogue. Si la boîte de dialogue a été spécifiée avec l’indicateur [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , cette notification retourne le pointeur vers le modèle de boîte de dialogue.

## <a name="remarks"></a>Remarques

Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur de **\_ MSGRESULT DWL** et retourner **true**. Par exemple :

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification PSN WIZNEXT est envoyé. Vous pouvez ajouter, insérer ou supprimer des pages en réponse à ces codes de notification, mais une attention particulière doit être prise si vous insérez ou supprimez des pages avant la page actuelle.

 

Si vous insérez ou supprimez des pages avant la page actuelle, vous devez retourner (via la **\_ MSGRESULT** de l’DWL) une valeur différente de zéro pour spécifier la nouvelle page souhaitée. Notez, toutefois, que si vous insérez ou supprimez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.

Pour cette raison, il est recommandé que les assistants qui ajoutent et suppriment des pages dynamiquement en réponse à PSN \_ WIZNEXT et [PSN \_ WIZBACK](psn-wizback.md) le fassent uniquement aux pages situées à la fin de la liste. Si vous souhaitez que votre Assistant supprime les pages avec précision, conservez les pages dynamiques à la fin de la liste et retournez aux pages permanentes avant de les supprimer.

Supposons, par exemple, qu’un Assistant se compose d’une page d’introduction, d’une série de pages dynamiques et d’une page de fin, et que vous souhaitez supprimer les pages dynamiques lorsque l’utilisateur atteint la page de fin.

1.  L’Assistant commence par deux pages : « introduction » et « fin ». L’utilisateur commence sur la page « Introduction ».
    1.  Introduction (l’utilisateur est ici)
    2.  Completion
2.  Lorsque l’utilisateur quitte l’introduction, l’Assistant ajoute les pages dynamiques et place l’utilisateur sur la première page dynamique en retournant (via l' **\_ MSGRESULT**) l’identificateur de boîte de dialogue de la page « dynamique 1 ». Dans cet exemple, il existe trois pages dynamiques.
    1.  Introduction
    2.  Completion
    3.  Dynamique 1 (l’utilisateur est ici)
    4.  Dynamique 2
    5.  Dynamique 3
3.  Une fois que l’utilisateur a navigué dans les pages dynamiques vers « Dynamic 3 », puis accède à la page suivante, l’application doit placer l’utilisateur sur la page « achèvement ». Là encore, cela se fait en retournant (via **DWL \_ MSGRESULT**) l’identificateur de boîte de dialogue de la page « achèvement ».
    1.  Introduction
    2.  Achèvement (l’utilisateur est ici)
    3.  Dynamique 1
    4.  Dynamique 2
    5.  Dynamique 3
4.  L’application peut ensuite supprimer les trois pages dynamiques (numérotées de trois à cinq) en toute sécurité.
    1.  Introduction
    2.  Achèvement (l’utilisateur est ici)

Notez que cette technique est nécessaire uniquement si votre Assistant supprime les pages dynamiquement. Si votre Assistant ajoute uniquement des pages dynamiquement, ce processus n’est pas nécessaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

