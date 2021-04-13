---
title: Message CB_SETLOCALE (winuser. h)
description: Une application envoie un \_ message CB SETLOCALE pour définir les paramètres régionaux actuels de la zone de liste déroulante. Si la zone de liste déroulante a le \_ style de tri CBS et que des chaînes sont ajoutées à l’aide \_ de CB ADDSTRING, les paramètres régionaux d’une zone de liste déroulante affectent le mode de tri des éléments de liste.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465930"
---
# <a name="cb_setlocale-message"></a>\_Message CB SETLOCALE

Une application envoie un message **CB \_ SETLOCALE** pour définir les paramètres régionaux actuels de la zone de liste déroulante. Si la zone de liste déroulante a le style de [**\_ Tri CBS**](combo-box-styles.md) et que des chaînes sont ajoutées à l’aide de [**CB \_ ADDSTRING**](cb-addstring.md), les paramètres régionaux d’une zone de liste déroulante affectent le mode de tri des éléments de liste.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’identificateur de paramètres régionaux pour la zone de liste déroulante à utiliser pour le tri lors de l’ajout de texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’identificateur de paramètres régionaux précédent. Si *wParam* spécifie des paramètres régionaux qui ne sont pas installés sur le système, la valeur de retour est CB \_ Err et les paramètres régionaux actuels de la zone de liste déroulante ne sont pas modifiés.

## <a name="remarks"></a>Notes

Utilisez la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) pour construire un identificateur de paramètres régionaux et la macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) pour construire un identificateur de langue. L’identificateur de langue est constitué d’un identificateur de langue primaire et d’un identificateur de sous-langue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**$ \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**\_GETLOCALE CB**](cb-getlocale.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

