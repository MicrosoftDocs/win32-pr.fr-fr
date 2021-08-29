---
title: Message TCM_HIGHLIGHTITEM (commctrl. h)
description: Définit l’état de surbrillance d’un élément d’onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b355b1a0ad4d228fc8f67051497b0327885f7cafc3860af9c74bac0812b344ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876509"
---
# <a name="tcm_highlightitem-message"></a>\_Message HIGHLIGHTITEM TCM

Définit l’état de surbrillance d’un élément d’onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **int** qui spécifie l’index de base zéro d’un élément de contrôle d’onglet.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **bool** spécifiant l’état de mise en surbrillance à définir. Si cette valeur est **true**, l’onglet est mis en surbrillance ; Si la **valeur est false**, l’onglet est défini sur son état par défaut. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Dans Comctl32.dll version 6,0, ce message n’a aucun effet visible lorsqu’un thème est actif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

