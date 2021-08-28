---
title: Message TB_CHECKBUTTON (commctrl. h)
description: Vérifie ou décoche un bouton donné dans une barre d’outils.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- TB_CHECKBUTTON les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec35b6a333e0663acc8c94dec22c2b8f4138cb6024b1f7919fd0ec73cdb0eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919129"
---
# <a name="tb_checkbutton-message"></a>TO \_ CHECKBUTTON message

Vérifie ou décoche un bouton donné dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton à vérifier.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut activer ou désactiver le bouton spécifié. Si la **valeur est true**, la vérification est ajoutée. Si la **valeur est false**, la vérification est supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Quand un bouton est activé, il est affiché dans un état appuyé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

