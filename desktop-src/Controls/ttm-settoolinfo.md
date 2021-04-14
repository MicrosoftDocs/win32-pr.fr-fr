---
title: Message TTM_SETTOOLINFO (commctrl. h)
description: Définit les informations gérées par un contrôle ToolTip pour un outil.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- TTM_SETTOOLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466798"
---
# <a name="ttm_settoolinfo-message"></a>\_Message atténuation SETTOOLINFO

Définit les informations gérées par un contrôle ToolTip pour un outil.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui spécifie les informations à définir. Le membre **cbSize** de cette structure doit être défini avant l’envoi de ce message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Certaines propriétés internes d’un outil sont établies lorsque l’outil est créé et ne sont pas recalculées lorsqu’un message **atténuation \_ SETTOOLINFO** est envoyé. Si vous affectez simplement des valeurs à une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) et que vous la transmettez au contrôle ToolTip avec un message **atténuation \_ SETTOOLINFO** , ces propriétés peuvent être perdues. Au lieu de cela, votre application doit d’abord demander la structure **TOOLINFO** actuelle de l’outil en envoyant le contrôle ToolTip à un message [**atténuation \_ GETTOOLINFO**](ttm-gettoolinfo.md) . Modifiez ensuite les membres de cette structure en fonction des besoins et repassez-la au contrôle ToolTip avec **atténuation \_ SETTOOLINFO**.

Lors de l’appel de **atténuation \_ SETTOOLINFO**, la chaîne vers laquelle pointe le membre **LpszText** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ne doit pas dépasser 80 **TCHARs** , y compris le caractère **null** de fin.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Atténuation \_ SETTOOLINFOW** (Unicode) et **atténuation \_ SETTOOLINFOA** (ANSI)<br/>           |



 

 





