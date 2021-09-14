---
title: Message TVM_GETUNICODEFORMAT (commctrl. h)
description: Récupère l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro GetUnicodeFormat TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- TVM_GETUNICODEFORMAT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115645"
---
# <a name="tvm_getunicodeformat-message"></a>TVM \_ GETUNICODEFORMAT message

Récupère l’indicateur de format de caractère Unicode pour le contrôle. Vous pouvez envoyer ce message explicitement ou utiliser la [**macro \_ GetUnicodeFormat TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’indicateur de format Unicode pour le contrôle. Si cette valeur est différente de zéro, le contrôle utilise des caractères Unicode. Si cette valeur est égale à zéro, le contrôle utilise des caractères ANSI.

## <a name="remarks"></a>Notes

Pour plus d’informations sur ce message, consultez les notes relatives à [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TVM \_ SETUNICODEFORMAT**](tvm-setunicodeformat.md)
</dt> </dl>

 

 





