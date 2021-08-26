---
title: Message LVM_SETGROUPINFO (commctrl. h)
description: Définit les informations de groupe.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO les contrôles de Windows de message
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
ms.openlocfilehash: 553a81c3cfe962ae6daf5ae4c988964028554bc662cec08df40c16fd8b4eb43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077269"
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

## <a name="remarks"></a>Remarques

Pour modifier l’ID de groupe d’un groupe existant, ajoutez <b>LVGF_GROUPID</b> à <b>LVGROUP. Mask</b> et définissez <b>LVGROUP. iGroupId</b> sur le nouvel ID. L’appel échoue si <b>LVGROUP. iGroupId</b> contient l’ID d’un groupe existant.

Pour mettre à jour d’autres propriétés d’un groupe existant (par exemple, mettre à jour un alignement du texte d’en-tête ou de pied de page pour le groupe, <b>uAlign</b>) <b>LVGROUP. Mask</b> ne doit pas contenir de <b>LVGF_GROUPID</b>, sinon la mise à jour échoue.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





