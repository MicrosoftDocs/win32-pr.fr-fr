---
title: Message PSM_SETBUTTONTEXT (Prsht. h)
description: Définit le texte d’un bouton dans un Assistant Aero. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032752"
---
# <a name="psm_setbuttontext-message"></a>\_Message PSM SETBUTTONTEXT

Définit le texte d’un bouton dans un Assistant Aero. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

L’une des valeurs suivantes spécifiant le bouton dont le texte est défini.



| Valeur                                                                                                                                                                                 | Signification                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_**</dt> </dl>                               | Bouton **précédent** .<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ Annuler**</dt> </dl>                         | Bouton **Annuler** .<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Bouton **Terminer** .<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ terminer**</dt> </dl>                         | Bouton **Terminer** .<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ suivant**</dt> </dl>                               | Bouton **suivant** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Texte à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





