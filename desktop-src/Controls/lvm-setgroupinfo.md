---
title: Message LVM_SETGROUPINFO (commctrl. h)
description: Définit les informations de groupe.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032350"
---
# <a name="lvm_setgroupinfo-message"></a>\_Message SETGROUPINFO LVM

Définit les informations de groupe. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>ID qui spécifie le groupe dont les informations doivent être définies.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Pointeur vers une structure [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) qui contient les informations à définir.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’ID du groupe en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Pour modifier l’ID de groupe d’un groupe existant, ajoutez <b>LVGF_GROUPID</b> à <b>LVGROUP. Mask</b> et définissez <b>LVGROUP. iGroupId</b> sur le nouvel ID. L’appel échoue si <b>LVGROUP. iGroupId</b> contient l’ID d’un groupe existant.

Pour mettre à jour d’autres propriétés d’un groupe existant (par exemple, mettre à jour un alignement du texte d’en-tête ou de pied de page pour le groupe, <b>uAlign</b>) <b>LVGROUP. Mask</b> ne doit pas contenir de <b>LVGF_GROUPID</b>, sinon la mise à jour échoue.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





