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
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999794"
---
# <a name="lvm_hasgroup-message"></a>\_Message HASGROUP LVM

Détermine si le contrôle d’affichage de liste possède un groupe spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>ID du groupe.</dd> <dt>

*lParam* 
</dt> <dd>Doit avoir la **valeur null**.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si le contrôle d’affichage de liste possède le groupe spécifié, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





