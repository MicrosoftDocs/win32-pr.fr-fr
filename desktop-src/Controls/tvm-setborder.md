---
title: Message TVM_SETBORDER (commctrl. h)
description: Définit la taille de la bordure pour les éléments dans un contrôle TreeView. Vous pouvez envoyer le message explicitement ou à l’aide de la \_ macro setBorder TreeView.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115609"
---
# <a name="tvm_setborder-message"></a>TVM \_ SETBORDER message

**Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.**

Définit la taille de la bordure pour les éléments dans un contrôle TreeView. Vous pouvez envoyer le message explicitement ou à l’aide de la macro [**\_ setBorder TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indicateurs d’action. Ce paramètre peut être une ou plusieurs des valeurs suivantes :



| Valeur                                                                                                                                                         | Signification                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Applique la taille de bordure spécifiée à gauche des éléments dans le contrôle TreeView. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Applique la taille de bordure spécifiée en haut des éléments dans le contrôle d’arborescence.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **short** qui spécifie la taille de la bordure gauche, en pixels. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **short** qui spécifie la taille de la bordure supérieure, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur de **type long** qui contient la taille de la bordure précédente, en pixels. Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la taille précédente de la bordure horizontale, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la taille précédente de la bordure verticale.

## <a name="remarks"></a>Notes

**Avertissement de sécurité :** L’utilisation de ce message peut compromettre la sécurité de votre programme.

La bordure de l’élément est définie uniquement à des fins d’espacement. Un paramètre réussi déclenche un recalcul des barres de défilement.

Ce message n’est peut-être pas pris en charge dans les versions ultérieures de Comctl32.dll. En outre, ce message n’est pas défini dans commctrl. h. Ajoutez les définitions suivantes aux fichiers sources de votre application pour utiliser le message :

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SetBorder TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

