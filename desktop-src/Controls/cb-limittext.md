---
title: Message CB_LIMITTEXT (winuser. h)
description: Limite la longueur du texte que l’utilisateur peut taper dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032847"
---
# <a name="cb_limittext-message"></a>\_Message LIMITTEXT CB

Limite la longueur du texte que l’utilisateur peut taper dans le contrôle d’édition d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre maximal de **TCHARs** que l’utilisateur peut entrer, à l’exclusion du caractère null de fin. Si ce paramètre est égal à zéro, la longueur du texte est limitée à 0x7FFFFFFE caractères.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est toujours **true**.

## <a name="remarks"></a>Notes

Si la zone de liste déroulante n’a pas le style [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , la définition de la limite du texte sur une valeur supérieure à la taille du contrôle d’édition n’a aucun effet.

Le **message \_ LIMITTEXT CB** limite uniquement le texte que l’utilisateur peut entrer. Elle n’a aucun effet sur le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni sur la longueur du texte copié dans le contrôle d’édition lorsqu’une chaîne de la zone de liste est sélectionnée.

La limite par défaut du texte qu’un utilisateur peut entrer dans le contrôle d’édition est 30 000 **TCHARs**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

 





