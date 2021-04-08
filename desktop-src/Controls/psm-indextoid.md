---
title: Message PSM_INDEXTOID (Prsht. h)
description: Prend l’index d’une page de feuille de propriétés et retourne son ID de ressource. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IndexToId.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033013"
---
# <a name="psm_indextoid-message"></a>\_Message PSM INDEXTOID

Prend l’index d’une page de feuille de propriétés et retourne son ID de ressource. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .

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

Retourne l’ID de ressource de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite. Sinon, elle retourne zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





