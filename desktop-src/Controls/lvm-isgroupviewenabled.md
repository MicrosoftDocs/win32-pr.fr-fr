---
title: Message LVM_ISGROUPVIEWENABLED (commctrl. h)
description: Vérifie si la vue de groupe est activée pour le contrôle d’affichage de liste.
ms.assetid: 7c6ffa1f-300c-4e5e-900f-93a41e06c951
keywords:
- LVM_ISGROUPVIEWENABLED les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_ISGROUPVIEWENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4934eb8f4b8dea9f31f589aab5e60798b83446cf0379ac7efbd4f1e67f5bef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079889"
---
# <a name="lvm_isgroupviewenabled-message"></a>\_Message ISGROUPVIEWENABLED LVM

Vérifie si la vue de groupe est activée pour le contrôle d’affichage de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la vue de groupe est activée, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





