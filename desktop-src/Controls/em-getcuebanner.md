---
title: Message EM_GETCUEBANNER (commctrl. h)
description: Obtient le texte affiché sous la forme d’une indication textuelle, ou Tip, dans un contrôle d’édition.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5a47811adcd13c0f2531bd645a9ea607dd68c4dd2c1154f226a54cf108b291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019717"
---
# <a name="em_getcuebanner-message"></a>\_Message GETCUEBANNER em

Obtient le texte affiché sous la forme d’une indication textuelle, ou Tip, dans un contrôle d’édition.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon Unicode qui reçoit le texte défini comme la file d’attente textuelle. L’appelant est chargé d’allouer la mémoire tampon.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon désignée par *wParam* dans **WCHARs**, y compris la **valeur null** de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modifier \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





