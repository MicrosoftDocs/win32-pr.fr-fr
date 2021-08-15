---
title: Message PSM_SETNEXTTEXT (Prsht. h)
description: Définit le texte du bouton suivant dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410079"
---
# <a name="psm_setnexttext-message"></a>\_Message PSM SETNEXTTEXT

Définit le texte du bouton **suivant** dans un Assistant. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucune valeur de retour significative.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





