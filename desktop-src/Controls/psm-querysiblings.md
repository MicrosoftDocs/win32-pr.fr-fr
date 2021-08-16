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
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088649"
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

## <a name="remarks"></a>Remarques

Si une page retourne une valeur différente de zéro, la feuille de propriétés n’envoie pas le message aux pages suivantes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





