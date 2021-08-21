---
title: Message PSM_INDEXTOPAGE (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son handle HPROPSHEETPAGE. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToPage.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- PSM_INDEXTOPAGE les contrôles de Windows de message
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
ms.openlocfilehash: 1f5cfe971ebdb85f444b20e66fcfaf77f87448f71b3a677bea104a5068daac9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078833"
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

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





