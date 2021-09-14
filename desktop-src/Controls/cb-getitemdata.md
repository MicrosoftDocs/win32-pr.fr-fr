---
title: Message CB_GETITEMDATA (winuser. h)
description: Une application envoie un \_ message GETITEMDATA CB à une zone de liste déroulante pour récupérer la valeur fournie par l’application associée à l’élément spécifié dans la zone de liste déroulante.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006830"
---
# <a name="cb_getitemdata-message"></a>\_Message GETITEMDATA CB

Une application envoie un **message \_ GETITEMDATA CB** à une zone de liste déroulante pour récupérer la valeur fournie par l’application associée à l’élément spécifié dans la zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l'élément.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est la valeur associée à l’élément. Si une erreur se produit, il s’agit de CB \_ Err.

Si l’élément se trouve dans une zone de liste déroulante owner-drawn créée sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur de retour est la valeur contenue dans le paramètre *lParam* du message [**CB \_ ADDSTRING**](cb-addstring.md) ou [**CB \_ INSERTSTRING**](cb-insertstring.md) , qui a ajouté l’élément à la zone de liste déroulante. Si le **style \_ HASSTRINGS CBS** n’a pas été utilisé, la valeur de retour est le paramètre *lParam* contenu dans un message [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

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

[**\_INSERTSTRING CB**](cb-insertstring.md)
</dt> <dt>

[**\_SETITEMDATA CB**](cb-setitemdata.md)
</dt> </dl>

 

 





