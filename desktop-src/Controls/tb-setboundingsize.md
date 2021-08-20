---
title: Message TB_SETBOUNDINGSIZE (commctrl. h)
description: Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d409769e08e489d922dbdc2361779953555000dca784a6f7b977bbbcd3a5e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167742"
---
# <a name="tb_setboundingsize-message"></a>TO \_ SETBOUNDINGSIZE message

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions ultérieures de Windows.\]

Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) dont le membre **CY** contient la hauteur englobante. Le membre **CX** (largeur) est ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="security-considerations"></a>Considérations relatives à la sécurité

L’utilisation de ce message peut compromettre la sécurité de votre programme.

## <a name="remarks"></a>Remarques

La taille limite contrôle la manière dont les boutons sont organisés en colonnes. Si le contrôle ToolBar n’a pas le style [**TBSTYLE \_ ex \_ Column**](toolbar-extended-styles.md) , ce message n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

