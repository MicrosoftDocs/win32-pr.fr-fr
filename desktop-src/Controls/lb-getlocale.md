---
title: Message LB_GETLOCALE (winuser. h)
description: Obtient les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le \_ style de tri lbs) et du texte ajouté par le \_ message lb ADDSTRING.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544519"
---
# <a name="lb_getlocale-message"></a>\_Message GETLOCALE lb

Obtient les paramètres régionaux actuels de la zone de liste. Vous pouvez utiliser les paramètres régionaux pour déterminer l’ordre de tri correct du texte affiché (pour les zones de liste avec le style de [**\_ Tri lbs**](list-box-styles.md) ) et du texte ajouté par le message [**lb \_ ADDSTRING**](lb-addstring.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour spécifie les paramètres régionaux actuels de la zone de liste. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient le code de pays/région et le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de langue.

## <a name="remarks"></a>Remarques

L’identificateur de langue se compose d’un identificateur de sous-langue et d’un identificateur de langue primaire. Utilisez la macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) pour extraire l’identificateur de langue primaire de la [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de la valeur de retour, et la macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) pour extraire l’identificateur de sous-langue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

