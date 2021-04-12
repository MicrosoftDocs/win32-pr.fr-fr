---
title: Message LVM_GETEMPTYTEXT (commctrl. h)
description: Obtient le texte à afficher lorsque le contrôle de liste s’affiche vide. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT les contrôles de message Windows
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
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464275"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





