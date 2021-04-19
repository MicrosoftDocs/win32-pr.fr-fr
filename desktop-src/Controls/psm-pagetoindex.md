---
title: Message PSM_PAGETOINDEX (Prsht. h)
description: Prend le handle HPROPSHEETPAGE de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet PageToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- PSM_PAGETOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513792"
---
# <a name="psm_pagetoindex-message"></a>\_Message PSM PAGETOINDEX

Prend le handle HPROPSHEETPAGE de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle HPROPSHEETPAGE vers la page de la feuille de propriétés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de base zéro de la page de feuille de propriétés spécifiée par *lParam* en cas de réussite. Sinon, retourne -1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





