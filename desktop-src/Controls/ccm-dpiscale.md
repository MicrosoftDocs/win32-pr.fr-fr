---
title: Message CCM_DPISCALE (commctrl. h)
description: Active la mise à l’échelle en points par pouce (dpi) automatique dans les contrôles de Tree-View, les contrôles de List-View, les contrôles ComboBoxEx, les contrôles d’en-tête, les boutons, les contrôles ToolBar, les contrôles d’animation et les listes d’images.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104518"
---
# <a name="ccm_dpiscale-message"></a>\_Message CCM DPISCALE

Active la mise à l’échelle en points par pouce (dpi) automatique dans [les contrôles d’affichage d’arborescence](tree-view-controls.md), [les contrôles de vue de liste](list-view-control-reference.md), les [contrôles ComboBoxEx](comboboxex-controls.md), les [contrôles d’en-tête](header-controls.md), les [boutons](buttons.md), les [contrôles ToolBar](toolbar-controls-overview.md), les [contrôles d’animation](animation-control-overview.md)et les [listes d’images](image-lists.md).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Affectez la valeur **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Notes

Le lancement rapide et la [barre des tâches](/windows/desktop/shell/taskbar) ne doivent pas spécifier de mise à l’échelle dpi, car les images sont déjà mises à l’échelle.

Tout contrôle qui utilise une liste d’images créée avec la métrique SmallIcon ne doit pas mettre à l’échelle ses icônes.

> [!Note]  
> Pour utiliser cette API, vous devez fournir un manifeste qui spécifie Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

