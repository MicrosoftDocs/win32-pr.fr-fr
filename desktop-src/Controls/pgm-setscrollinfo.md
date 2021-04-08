---
title: Message PGM_SETSCROLLINFO (commctrl. h)
description: Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de radiomessagerie \_ SetScrollInfo.
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843426"
---
# <a name="pgm_setscrollinfo-message"></a>\_Message SETSCROLLINFO PGM

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]

Définit les paramètres de défilement du contrôle de pagineur, y compris la valeur du délai d’attente, les lignes par délai d’attente et les pixels par ligne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro de [**radiomessagerie \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

**Uint** qui spécifie la valeur de délai d’attente pour le défilement, en millisecondes.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **uint** qui spécifie le nombre de lignes à faire défiler par délai d’attente. Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **uint** qui spécifie le nombre de pixels par ligne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Notes

La valeur *wParam* Timeout contrôle la vitesse à laquelle le contrôle de pagineur génère des événements de défilement lorsque le contrôle a capturé l’entrée de la souris et que le bouton gauche de la souris est enfoncé. Des valeurs plus petites entraînent un défilement plus rapide ; des valeurs plus élevées entraînent un défilement plus lent. La valeur par défaut est un huitième de la durée du double-clic. Pour plus d’informations, consultez [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime).

Par défaut, à chaque événement de défilement, le contrôle de pagineur fait défiler un montant égal à la largeur ou à la hauteur entière du contrôle, selon que le contrôle de pagineur a une orientation horizontale ou verticale. Les valeurs de *lParam* sont utilisées pour remplacer la valeur de défilement par défaut. Si les valeurs autres que zéro sont fournies, la valeur de défilement est le produit des deux valeurs (LOWORD (*lParam*) \* HIWORD (*lParam*)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Radiomessagerie \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

