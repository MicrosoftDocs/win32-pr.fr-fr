---
title: Message CBEM_SETIMAGELIST (commctrl. h)
description: Définit une liste d’images pour un contrôle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699259"
---
# <a name="cbem_setimagelist-message"></a>\_Message CBEM SETIMAGELIST

Définit une liste d’images pour un contrôle ComboBoxEx.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images à définir pour le contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images précédemment associée au contrôle, ou retourne la **valeur null** si aucune liste d’images n’a été définie précédemment.

## <a name="remarks"></a>Remarques

> [!IMPORTANT]
> La hauteur des images de votre liste d’images peut modifier les exigences de taille du contrôle ComboBoxEx. Il est recommandé de redimensionner le contrôle après l’envoi de ce message pour vous assurer qu’il s’affiche correctement.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





