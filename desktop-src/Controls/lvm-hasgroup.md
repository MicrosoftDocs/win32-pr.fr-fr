---
title: Message LVM_HASGROUP (commctrl. h)
description: Détermine si le contrôle d’affichage de liste possède un groupe spécifié.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9dcfadf3e7a07a5f814f5421ed97d26faff6a5ac4c36ce97b9faea77c6a152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293739"
---
# <a name="lvm_hasgroup-message"></a>\_Message HASGROUP LVM

Détermine si le contrôle d’affichage de liste possède un groupe spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>ID du groupe.</dd> <dt>

*lParam* 
</dt> <dd>Doit avoir la **valeur null**.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le contrôle d’affichage de liste possède le groupe spécifié, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





