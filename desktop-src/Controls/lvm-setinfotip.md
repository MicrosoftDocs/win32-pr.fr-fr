---
title: Message LVM_SETINFOTIP (commctrl. h)
description: Définit le texte info-bulle en réponse différée à la \_ notification LVN GETINFOTIP.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312685"
---
# <a name="lvm_setinfotip-message"></a>\_Message SETINFOTIP LVM

Définit le texte info-bulle en réponse différée à la notification [LVN \_ GETINFOTIP](lvn-getinfotip.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> qui contient les informations à définir.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si le texte de l’info-bulle est correctement défini, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Le **message \_ SETINFOTIP LVM** permet à une application de calculer info-bulles en arrière-plan en effectuant les étapes suivantes :

1.  En réponse à la notification [LVN \_ GETINFOTIP](lvn-getinfotip.md) , définissez le membre **PszText** de la structure [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) sur une chaîne vide et retournez 0.
2.  En arrière-plan, calculez l’info-bulle.
3.  Après le calcul de l’info-bulle, envoyez le message **\_ SETINFOTIP LVM** , en définissant le membre **PszText** de la structure [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sur l’info-bulle et les membres **iItem** et **iSubItem** sur l’élément et le sous-élément auxquels s’applique l’info-bulle.

Le texte transmis au message **LVM \_ SETINFOTIP** s’affiche uniquement si l’élément et le sous-élément décrits par la structure [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sont toujours dans un État qui requiert une info-bulle

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





