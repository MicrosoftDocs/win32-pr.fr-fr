---
title: Message LVM_SETCOLUMNWIDTH (commctrl. h)
description: Modifie la largeur d’une colonne en mode rapport ou la largeur de toutes les colonnes en mode affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetColumnWidth.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102892"
---
# <a name="lvm_setcolumnwidth-message"></a>\_Message SETCOLUMNWIDTH LVM

Modifie la largeur d’une colonne en mode rapport ou la largeur de toutes les colonnes en mode affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro d’une colonne valide. Pour le mode affichage de liste, ce paramètre doit avoir la valeur zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Nouvelle largeur de la colonne, en pixels. Pour le mode rapport-vue, les valeurs spéciales suivantes sont prises en charge :



| Valeur                                                                                                                                                                                           | Signification                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**\_REdimensionnement automatique LVSCW**</dt> </dl>                                | Dimensionne automatiquement la colonne.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AutoSize \_ USEHEADER**</dt> </dl> | Dimensionne automatiquement la colonne pour qu’elle corresponde au texte d’en-tête. Si vous utilisez cette valeur avec la dernière colonne, sa largeur est définie pour remplir la largeur restante du contrôle de vue de liste.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Supposons que vous disposez d’un contrôle de vue de liste de 2 colonnes avec une largeur de 500 pixels. Si la largeur de la colonne zéro est définie sur 200 pixels, et que vous envoyez ce message avec *wParam* = 1 et *lParam* = LVSCW \_ AutoSize \_ USEHEADER, la deuxième colonne (et la dernière) aura une largeur de 300 pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





