---
title: Message PSM_SETTITLE (Prsht. h)
description: Définit le titre d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetTitle.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- PSM_SETTITLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941707"
---
# <a name="psm_settitle-message"></a>\_Message PSM SETTITLE

Définit le titre d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateur qui spécifie s’il faut inclure le préfixe « Properties for » ou le suffixe « Properties » (selon la version) avec la chaîne de titre spécifiée. Si cette valeur est PSH \_ PROPTITLE, le préfixe ou le suffixe est inclus.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la chaîne de titre. Si le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de ce paramètre a la **valeur null**, la feuille de propriétés charge la ressource de type chaîne spécifiée dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Dans un Assistant Aero, ce message peut être utilisé pour modifier le titre d’une page intérieure de manière dynamique ; par exemple, lors de la gestion de la notification [ \_ SetActive PSN](psn-setactive.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **PSM \_ SETTITLEW** (Unicode) et **PSM \_ SETTITLEA** (ANSI)<br/>              |



 

