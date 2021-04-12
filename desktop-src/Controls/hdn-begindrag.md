---
title: HDN_BEGINDRAG le code de notification (commctrl. h)
description: Envoyé par un contrôle header lorsqu’une opération glisser a commencé sur l’un de ses éléments. Ce code de notification est uniquement envoyé par les contrôles Header définis sur le \_ style HDS DRAGDROP. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Contrôles Windows de code de notification HDN_BEGINDRAG
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032792"
---
# <a name="hdn_begindrag-notification-code"></a>\_Code de notification HDN BEGINDRAG

Envoyé par un contrôle header lorsqu’une opération glisser a commencé sur l’un de ses éléments. Ce code de notification est uniquement envoyé par les contrôles Header définis sur le style [**HDS \_ DRAGDROP**](header-control-styles.md) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenant des informations sur l’élément d’en-tête qui est glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour permettre au contrôle header de gérer automatiquement les opérations de glisser-déplacer, retournez **false**. Si le propriétaire du contrôle effectue manuellement la réorganisation par glisser-déplacer, retourne la **valeur true**.

## <a name="remarks"></a>Notes

Par défaut, un contrôle header gère automatiquement la réorganisation des opérations de glisser-déplacer. Le retour de la **valeur true** pour indiquer que la gestion du glisser-déplacer externe (manuelle) permet au propriétaire du contrôle de fournir des services personnalisés dans le cadre du processus de glisser-déplacer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





