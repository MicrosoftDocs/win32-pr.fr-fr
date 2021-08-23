---
title: PSN_APPLY le code de notification (Prsht. h)
description: Envoyé à chaque page de la feuille de propriétés pour indiquer que l’utilisateur a cliqué sur le bouton OK, fermer ou appliquer et souhaite que toutes les modifications soient prises en compte. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d4a0ea52f4cee495e689e8f0cdc91d7362ec3a1ee37ab81a911bc980d3209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410035"
---
# <a name="psn_apply-notification-code"></a>PSN \_ appliquer le code de notification

Envoyé à chaque page de la feuille de propriétés pour indiquer que l’utilisateur a cliqué sur le bouton OK, fermer ou appliquer et souhaite que toutes les modifications soient prises en compte. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification, y compris l’ID de la page.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Définissez PSNRET \_ NOERROR pour indiquer que les modifications apportées à cette page sont valides et ont été appliquées. Si toutes les pages définissent PSNRET \_ NOERROR, la feuille de propriétés peut être détruite. Pour indiquer que les modifications apportées à cette page ne sont pas valides et que la feuille de propriétés n’est pas détruite, définissez l’une des valeurs de retour suivantes :

-   PSNRET \_ non valide. La feuille de propriétés ne sera pas détruite et le focus sera renvoyé à cette page.
-   PSNRET \_ non valide \_ NOCHANGEPAGE. La feuille de propriétés ne sera pas détruite et le focus sera retourné à la page qui avait le focus lorsque le bouton était enfoncé.

Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la \_ valeur de MSGRESULT DWL, et la procédure de boîte de dialogue doit retourner **true**.

## <a name="remarks"></a>Remarques

Quand l’utilisateur clique sur le bouton OK, appliquer ou fermer, la feuille de propriétés envoie une notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page active, ce qui lui donne la possibilité de valider les modifications de l’utilisateur. Si les modifications sont valides, la feuille de propriétés envoie un \_ Code de notification d’application PSN à chaque page, en la dirigeant pour appliquer les nouvelles propriétés à l’élément correspondant.

> [!Note]  
> La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification d’application PSN est envoyé. N’essayez pas d’ajouter, de supprimer ou d’insérer des pages pendant la gestion de cette notification. Vous obtiendrez des résultats imprévisibles.

 

Le membre **lParam** de la structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) vers laquelle pointe *lParam* prend la valeur **true** si l’utilisateur clique sur le bouton OK. Elle est également définie sur **true** si le message [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) a été envoyé et que l’utilisateur clique sur le bouton Fermer. Elle a la valeur **false** si l’utilisateur clique sur le bouton appliquer.

La structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.

N’appelez pas la fonction [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) lors du traitement de ce code de notification.

Une feuille de propriétés modale est détruite si l’utilisateur clique sur le bouton OK et que chaque page retourne la \_ valeur d’erreur noPSNRET en réponse à **PSN \_ apply**. Si une page retourne un \_ NOCHANGEPAGE non valide PSNRET ou PSNRET \_ non valide \_ , le processus d’application est immédiatement annulé. Les pages après la page d’annulation ne recevront pas de \_ Code de notification d’application PSN.

Pour recevoir ce code de notification, une page doit définir la \_ valeur DWL MSGRESULT sur **false** en réponse au code de notification [PSN \_ KILLACTIVE](psn-killactive.md) .

> [!Note]  
> Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

