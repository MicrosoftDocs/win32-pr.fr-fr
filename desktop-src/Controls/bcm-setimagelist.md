---
title: Message BCM_SETIMAGELIST (commctrl. h)
description: Assigne une liste d’images à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ SetImageList macro.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920396"
---
# <a name="bcm_setimagelist-message"></a>\_Message SETIMAGELIST BCM

Assigne une liste d’images à un contrôle bouton. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**\_ IMAGELIST de bouton**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) qui contient des informations sur la liste d’images.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

La liste d’images référencée dans le membre **himl** de la structure [**\_ IMAGELIST Button**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) doit contenir une seule image à utiliser pour tous les États ou des images individuelles pour chaque État. Les États suivants sont définis dans vssym32. h.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Notez que PBS \_ STYLUSHOT est utilisé uniquement sur les Tablet PC.

Chaque valeur est un index de l’image appropriée dans la liste d’images. Si une seule image est présente, elle est utilisée pour tous les États. Si la liste d’images contient plus d’une image, chaque index correspond à un État du bouton. Si aucune image n’est fournie pour chaque État, rien n’est dessiné pour ces États sans images.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





