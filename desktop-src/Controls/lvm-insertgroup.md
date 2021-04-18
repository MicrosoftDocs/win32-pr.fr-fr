---
title: Message LVM_INSERTGROUP (commctrl. h)
description: Insère un groupe dans un contrôle List-View.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP les contrôles de message Windows
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
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511962"
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

## <a name="remarks"></a>Notes

Pour activer le mode groupe, appelez [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) ou [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).

Un groupe ne peut pas être inséré dans un contrôle d’affichage de liste vide.

Veillez à définir le **iGroupId** dans le ou les éléments auxquels le groupe a été ajouté. Sinon, après le traitement du message [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) avec **true** , le contrôle ListView n’affichera aucun élément.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant la version 6,0 de Comclt32. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





