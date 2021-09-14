---
title: Message TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Démarre et arrête l’affichage du texte défilant de la barre de progression dans une boîte de dialogue de tâche et définit la vitesse du texte défilant.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116073"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>\_Message de \_ \_ \_ texte défilant de la barre de progression TDM Set

Démarre et arrête l’affichage du texte défilant de la barre de progression dans une boîte de dialogue de tâche et définit la vitesse du texte défilant.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui indique s’il faut activer ou désactiver l’affichage du texte défilant. Utilisez **true** pour activer l’affichage du texte défilant ou **false** pour le désactiver.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

**Uint** qui spécifie le temps, en millisecondes, entre les mises à jour de l’animation de texte défilant. Si ce paramètre est égal à zéro, l’animation de texte défilant est mise à jour toutes les 30 millisecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Pour plus d’informations sur le mode texte défilant, consultez [contrôle de barre de progression](progress-bar-control.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





