---
title: Message LVM_SETVIEW (commctrl. h)
description: Définit l’affichage d’un contrôle List-View.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8d07b636a14624632d0e41ebcf6db66f420b9df4f8ca852e55ab2f3e1578e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656199"
---
# <a name="lvm_setview-message"></a>\_Message SETVIEW LVM

Définit l’affichage d’un contrôle List-View.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>**Valeur DWORD** qui spécifie la vue.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 1 en cas de réussite, ou-1 dans le cas contraire. Par exemple,-1 est retourné si la vue n’est pas valide.

## <a name="remarks"></a>Remarques

Voici les valeurs des vues.

-   Détails de la \_ vue LV \_
-   \_icône de vue LV \_
-   \_liste d’affichages LV \_
-   LV \_ vue \_ SmallIcon
-   vignette de la \_ vue LV \_

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comctl32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





