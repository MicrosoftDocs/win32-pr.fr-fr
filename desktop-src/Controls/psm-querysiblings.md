---
title: Message PSM_QUERYSIBLINGS (Prsht. h)
description: Envoyé à une feuille de propriétés, qui transfère ensuite le message à chacune de ses pages. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117482"
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

## <a name="return-value"></a>Valeur de retour

Retourne la valeur différente de zéro d’une page de la feuille de propriétés, ou zéro si aucune page ne retourne une valeur différente de zéro.

## <a name="remarks"></a>Notes

Si une page retourne une valeur différente de zéro, la feuille de propriétés n’envoie pas le message aux pages suivantes.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





