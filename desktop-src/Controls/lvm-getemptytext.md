---
title: Message LVM_GETEMPTYTEXT (commctrl. h)
description: Obtient le texte à afficher lorsque le contrôle de liste s’affiche vide. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dd1dc1df7b0a558adda37938849b5383bbfee304d807a22a329e4f7301889b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411468"
---
# <a name="lvm_getemptytext-message"></a>\_Message GETEMPTYTEXT LVM

Obtient le texte à afficher lorsque le contrôle de liste s’affiche vide. Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe *lParam*, y compris le caractère **null** de fin.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Pointeur vers une mémoire tampon Unicode, terminée par un caractère null, de taille spécifiée par *wParam* pour recevoir le texte. L’appelant est chargé d’allouer la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





