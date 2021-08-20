---
title: Message HDM_EDITFILTER (commctrl. h)
description: Déplace le focus d’entrée vers la zone d’édition lorsqu’un bouton de filtre a le focus.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8636c17bfa9043891e5037df79be9c72c1ddc8f3aa2b4d13520f4289205b5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006159"
---
# <a name="hdm_editfilter-message"></a>\_Message HDM EDITFILTER

Déplace le focus d’entrée vers la zone d’édition lorsqu’un bouton de filtre a le focus.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur qui spécifie la colonne à modifier.

</dd> <dt>

*lParam* 
</dt> <dd>

Indicateur qui spécifie comment gérer les modifications de modification de l’utilisateur. Utilisez cet indicateur pour spécifier la procédure à suivre si l’utilisateur est en train de modifier le filtre lorsque le message est envoyé.



| Valeur                                                                                                                                      | Signification                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt></dt><dt> **True**</dt> </dl>  | Ignorez les modifications apportées par l’utilisateur. <br/> |
| <dl> <dt></dt><dt> **Valeur false**</dt> </dl> | Accepter les modifications apportées par l’utilisateur. <br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un entier. La propriété **LRESULT** est castée en un entier qui indique **true**(1) ou **false**(0).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HDM \_ CLEARFILTER**](hdm-clearfilter.md)
</dt> </dl>

 

 





