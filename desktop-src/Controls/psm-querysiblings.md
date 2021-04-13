---
title: Message PSM_QUERYSIBLINGS (Prsht. h)
description: Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508701"
---
# <a name="psm_querysiblings-message"></a>\_Message PSM QUERYSIBLINGS

Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Premier paramètre défini par l’application.

</dd> <dt>

*lParam* 
</dt> <dd>

Deuxième paramètre défini par l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur différente de zéro d’une page de la feuille de propriétés, ou zéro si aucune page ne retourne une valeur différente de zéro.

## <a name="remarks"></a>Notes

Si une page retourne une valeur différente de zéro, la feuille de propriétés n’envoie pas le message aux pages suivantes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





