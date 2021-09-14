---
title: Message PSM_HWNDTOINDEX (Prsht. h)
description: Prend le handle de fenêtre de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117517"
---
# <a name="psm_hwndtoindex-message"></a>\_Message PSM HWNDTOINDEX

Prend le handle de fenêtre de la page de la feuille de propriétés et retourne son index de base zéro. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de la page.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de base zéro de la page de feuille de propriétés spécifiée par *wParam* en cas de réussite. Sinon, retourne -1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





