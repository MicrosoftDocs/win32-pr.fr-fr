---
title: Message LVM_SETCOLUMNWIDTH (commctrl. h)
description: Modifie la largeur d’une colonne en mode rapport ou la largeur de toutes les colonnes en mode affichage de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetColumnWidth.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH les contrôles de Windows de message
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
ms.openlocfilehash: 7a127706d6a47444ee59f1434478aadb5170f9ac7a919dca6fd6151de33486d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077289"
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

## <a name="remarks"></a>Remarques

Supposons que vous disposez d’un contrôle de vue de liste de 2 colonnes avec une largeur de 500 pixels. Si la largeur de la colonne zéro est définie sur 200 pixels, et que vous envoyez ce message avec *wParam* = 1 et *lParam* = LVSCW \_ AutoSize \_ USEHEADER, la deuxième colonne (et la dernière) aura une largeur de 300 pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





