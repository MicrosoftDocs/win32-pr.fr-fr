---
title: Message CBEM_HASEDITCHANGED (commctrl. h)
description: Détermine si l’utilisateur a modifié le texte d’un contrôle d’édition ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942852"
---
# <a name="cbem_haseditchanged-message"></a>\_Message CBEM HASEDITCHANGED

Détermine si l’utilisateur a modifié le texte d’un contrôle d’édition ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le texte de la zone d’édition du contrôle a été modifié, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Un contrôle ComboBoxEx utilise un contrôle de zone d’édition lorsqu’il est défini sur le style de [**\_ liste déroulante CBS**](combo-box-styles.md) . Vous pouvez récupérer le handle de fenêtre du contrôle de zone d’édition en envoyant un message [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .

Lorsque l’utilisateur commence à modifier, vous recevrez une notification [CBEN \_ BEGINEDIT](cben-beginedit.md) . Une fois la modification terminée ou le focus modifié, vous recevrez une notification [CBEN \_ ENDEDIT](cben-endedit.md) . Le message **CBEM \_ HASEDITCHANGED** n’est utile que pour déterminer si le texte a été modifié s’il est envoyé avant la \_ notification CBEN ENDEDIT. Si le message est envoyé par la suite, la **valeur false** est retournée. Par exemple, supposons que l’utilisateur commence à modifier le texte dans la zone d’édition, mais qu’il change le focus, générant une \_ notification CBEN ENDEDIT. Si vous envoyez ensuite un message **CBEM \_ HASEDITCHANGED** , la **valeur false** est retournée, même si le texte a été modifié.

Le [**style \_ simple CBS**](combo-box-styles.md) ne fonctionne pas correctement avec **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





