---
title: Message LVM_ENABLEGROUPVIEW (commctrl. h)
description: Active ou désactive si les éléments d’un contrôle List View s’affichent en tant que groupe.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848bf348a35ee171f23e499464b65c847b67f920c53175fcf920d56e7e30fb90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698779"
---
# <a name="lvm_enablegroupview-message"></a>\_Message ENABLEGROUPVIEW LVM

Active ou désactive si les éléments d’un contrôle List View s’affichent en tant que groupe.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Valeur **booléenne** qui indique s’il faut activer un contrôle d’affichage de liste pour regrouper les éléments affichés. Utilisez **true** pour activer le regroupement, **false** pour le désactiver. </dd> <dt>

*lParam* 
</dt> <dd>Doit avoir la **valeur null**.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs suivantes.



| Code de retour                                                                       | Description                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**entre**</dt> </dl>  | La possibilité d’afficher des éléments de vue liste en tant que groupe est déjà activée ou désactivée.<br/> |
| <dl> <dt>**1**</dt> </dl>  | L’état du contrôle a été correctement modifié.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | L'opération a échoué.<br/>                                                             |



 

## <a name="remarks"></a>Remarques

**LVM \_ ENABLEGROUPVIEW** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





