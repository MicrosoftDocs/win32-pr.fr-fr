---
title: Message CBEM_SETIMAGELIST (commctrl. h)
description: Définit une liste d’images pour un contrôle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST les contrôles de message Windows
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
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942769"
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

## <a name="remarks"></a>Notes

> [!IMPORTANT]
> La hauteur des images de votre liste d’images peut modifier les exigences de taille du contrôle ComboBoxEx. Il est recommandé de redimensionner le contrôle après l’envoi de ce message pour vous assurer qu’il s’affiche correctement.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





