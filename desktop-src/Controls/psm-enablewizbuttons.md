---
title: Message PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Active ou désactive tous les boutons standard dans un Assistant Aero. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet EnableWizButtons.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942378"
---
# <a name="psm_enablewizbuttons-message"></a>\_Message PSM ENABLEWIZBUTTONS

Active ou désactive tous les boutons standard dans un Assistant Aero. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Une ou plusieurs des valeurs suivantes qui spécifient les boutons de la feuille de propriétés qui doivent être activés. Si une valeur de bouton est incluse à la fois dans ce paramètre et dans *lParam*, elle est activée.



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

Une ou plusieurs des valeurs utilisées dans *wParam*, en spécifiant les boutons affectés par cet appel. Si une valeur de bouton apparaît dans ce paramètre mais pas dans *wParam*, elle indique que le bouton doit être désactivé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





