---
description: Demande l’autorisation de suspendre l’ordinateur. Une application qui accorde cette autorisation doit effectuer des opérations de préparation à la mise en veille avant de retourner sa réponse.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Événement PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865073"
---
# <a name="pbt_apmquerysuspend-event"></a>\_Événement PBT APMQUERYSUSPEND

\[PBT \_ APMQUERYSUSPEND peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. La prise en charge de cet événement a été supprimée dans Windows Vista. Utilisez [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) à la place.\]

Demande l’autorisation de suspendre l’ordinateur. Une application qui accorde cette autorisation doit effectuer des opérations de préparation à la mise en veille avant de retourner sa réponse.

Une fenêtre reçoit cet événement par le biais du message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) . Les paramètres *wParam* et *lParam* sont définis comme suit.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>*uMsg*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                                                   | Signification                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Identificateur du message.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Valeur                                                                                                                                                                                                                                        | Signification                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | Identificateur d’événement.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Indicateurs d’action. Si le bit 0 est 1, l’application peut inviter l’utilisateur à fournir des instructions sur la façon de se préparer à la suspension. dans le cas contraire, l’application doit se préparer sans intervention de l’utilisateur. Toutes les autres valeurs de bit sont réservées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour autoriser l’interruption de la demande. Pour refuser la demande, retournez **la \_ requête \_ de diffusion Deny**.

## <a name="remarks"></a>Notes

Une application doit traiter cet événement aussi rapidement que possible. L’application peut demander à l’utilisateur des instructions sur la façon de se préparer à la suspension uniquement si le bit 0 dans le paramètre *Flags* est défini. Toutefois, si ce message est émis parce que l’utilisateur ferme le couvercle de l’ordinateur portable, il ne sera pas possible d’inviter l’utilisateur. Les applications doivent respecter un certain comportement lorsqu’elles ferment le couvercle de l’ordinateur portable ou appuient sur le bouton d’alimentation et permettent à la transition de s’effectuer correctement.

Le système laisse environ 20 secondes à une application de supprimer le message [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) qui envoie l’événement PBT \_ APMQUERYSUSPEND à partir de la file d’attente des messages de l’application. Si une application ne supprime pas le message de sa file d’attente en moins de 20 secondes, le système suppose que l’application est dans un État non réactif et que l’application accepte la demande de mise en veille. Les opérations des applications qui ne traitent pas leurs files d’attente de messages peuvent être interrompues. Une fois que le message a été supprimé de la file d’attente de messages, une application peut prendre autant de temps que nécessaire pour effectuer les opérations requises avant d’entrer dans l’état de veille. Toutes les opérations qui peuvent durer plus de 20 secondes doivent être effectuées pour l’instant, car le système n’autorise que 20 secondes pour que les opérations se terminent au cours du traitement [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                                           |
| En-tête<br/>                   | <dl> <dt>WinUser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de mise en éveil du système](system-wake-up-events.md)
</dt> <dt>

[Événements de gestion de l’alimentation](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**\_POWERBROADCAST WM**](wm-powerbroadcast.md)
</dt> </dl>

 

 




