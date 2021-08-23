---
title: Message LVM_INSERTGROUP (commctrl. h)
description: Insère un groupe dans un contrôle List-View.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f31504226663b0df91e0297ed29abf784ff239dfcee5f323e8617f73dff65acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019247"
---
# <a name="lvm_insertgroup-message"></a>\_Message INSERTGROUP LVM

Insère un groupe dans un contrôle List-View.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Index où le groupe doit être ajouté. S’il s’agit de-1, le groupe est ajouté à la fin de la liste.</dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> qui contient le groupe à ajouter.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément auquel le groupe a été ajouté, ou-1 si l’opération a échoué.

## <a name="remarks"></a>Remarques

Pour activer le mode groupe, appelez [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) ou [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Un groupe ne peut pas être inséré dans un contrôle d’affichage de liste vide.

Veillez à définir le **iGroupId** dans le ou les éléments auxquels le groupe a été ajouté. Sinon, après le traitement du message [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) avec **true** , le contrôle ListView n’affichera aucun élément.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant la version 6,0 de Comclt32. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





