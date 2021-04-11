---
title: Message PSM_IDTOINDEX (Prsht. h)
description: Prend l’ID de ressource d’une page de feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet IdToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- PSM_IDTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105274"
---
# <a name="psm_idtoindex-message"></a>\_Message PSM IDTOINDEX

Prend l’ID de ressource d’une page de feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

ID de ressource de la page.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de base zéro de la page de feuille de propriétés spécifiée par *lParam* en cas de réussite. Sinon, retourne -1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





