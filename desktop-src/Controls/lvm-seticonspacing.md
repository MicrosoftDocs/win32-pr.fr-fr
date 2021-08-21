---
title: Message LVM_SETICONSPACING (commctrl. h)
description: Définit l’espacement entre les icônes des contrôles d’affichage de liste qui ont le \_ style d’icône LVS. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetIconSpacing.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019176"
---
# <a name="lvm_seticonspacing-message"></a>\_Message SETICONSPACING LVM

Définit l’espacement entre les icônes des contrôles d’affichage de liste qui ont le style d' [**\_ icône LVS**](list-view-window-styles.md) . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la distance, en pixels, à définir entre les icônes sur l’axe des abscisses. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la distance, en pixels, à définir entre les icônes sur l’axe des ordonnées. Consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **DWORD** qui contient la distance précédente de l’axe x dans le mot bas, et la distance de l’axe y précédente dans le mot haut.

## <a name="remarks"></a>Remarques

Les valeurs de *lParam* sont relatives à l’angle supérieur gauche d’une image bitmap. Par conséquent, pour définir l’espacement entre les icônes qui ne se chevauchent pas, les valeurs *lParam* doivent inclure la taille de l’icône, plus la quantité d’espace vide souhaitée entre les icônes. Les valeurs qui n’incluent pas la largeur de l’icône entraînent des chevauchements.

Lors de la définition de l’espacement des icônes, les valeurs *lParam* doivent être définies à 4 ou plus. Les valeurs inférieures ne produisent pas la disposition souhaitée. Pour réinitialiser les icônes à l’espacement par défaut, affectez la valeur-1 aux valeurs *lParam* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

