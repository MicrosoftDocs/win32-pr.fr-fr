---
title: Message CB_SETITEMDATA (winuser. h)
description: Une application envoie un \_ message CB SETITEMDATA pour définir la valeur associée à l’élément spécifié dans une zone de liste déroulante.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120066"
---
# <a name="cb_setitemdata-message"></a>\_Message SETITEMDATA CB

Une application envoie un message **CB \_ SETITEMDATA** pour définir la valeur associée à l’élément spécifié dans une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’index de base zéro de l’élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie la nouvelle valeur à associer à l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une erreur se produit, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

Si l’élément spécifié se trouve dans une zone de liste déroulante owner-drawn créée sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , ce message remplace la valeur dans le paramètre *lParam* du message [**CB \_ ADDSTRING**](cb-addstring.md) ou [**CB \_ INSERTSTRING**](cb-insertstring.md) qui a ajouté l’élément à la zone de liste déroulante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_GETITEMDATA CB**](cb-getitemdata.md)
</dt> <dt>

[**\_INSERTSTRING CB**](cb-insertstring.md)
</dt> </dl>

 

 





