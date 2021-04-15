---
title: Message PSM_INDEXTOPAGE (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466323"
---
# <a name="psm_indextopage-message"></a>\_Message PSM INDEXTOPAGE

Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la page.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle HPROPSHEETPAGE de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite. Sinon, elle retourne zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





