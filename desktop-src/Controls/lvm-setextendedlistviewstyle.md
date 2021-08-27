---
title: Message LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Définit des styles étendus dans les contrôles d’affichage de liste. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro ListView SetExtendedListViewStyle ou ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077279"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>\_Message SETEXTENDEDLISTVIEWSTYLE LVM

Définit des styles étendus dans les contrôles d’affichage de liste. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) ou [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur **DWORD** qui spécifie les styles de *lParam* à affecter. Ce paramètre peut être une combinaison de [**styles de List-View étendus**](extended-list-view-styles.md). Seuls les styles étendus dans *wParam* seront modifiés. Tous les autres styles seront conservés tels quels. Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur **DWORD** qui spécifie les styles de contrôle de vue de liste étendus à définir. Ce paramètre peut être une combinaison de [**styles de List-View étendus**](extended-list-view-styles.md). Les styles qui ne sont pas définis, mais qui sont spécifiés dans *wParam*, sont supprimés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient les styles de contrôle de vue de liste étendus précédents.

## <a name="remarks"></a>Remarques

Le paramètre *wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants. Par exemple, si vous transmettez [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) pour *wParam* et 0 pour *lParam*, le style **LVS \_ ex \_ FULLROWSELECT** sera effacé, mais tous les autres styles resteront les mêmes.

Pour des raisons de compatibilité descendante, la macro [**\_ SetExtendedListViewStyle ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) n’a pas été mise à jour pour utiliser *wParam*. Pour utiliser la valeur *wParam* , utilisez la macro [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

Lorsque vous utilisez ce message pour définir le style de [**\_ cases à \_ cocher LVS ex**](extended-list-view-styles.md) , tout index d’image d’état précédemment défini sera ignoré. Toutes les cases à cocher seront initialisées à l’état non vérifié. L’index d’image d’État est contenu dans les bits 12 à 15 du membre d' **État** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





