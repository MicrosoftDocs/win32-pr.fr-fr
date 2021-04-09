---
title: Message TB_SETBOUNDINGSIZE (commctrl. h)
description: Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE les contrôles de message Windows
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
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843057"
---
# <a name="tb_setboundingsize-message"></a>TO \_ SETBOUNDINGSIZE message

\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]

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

## <a name="remarks"></a>Notes

La taille limite contrôle la manière dont les boutons sont organisés en colonnes. Si le contrôle ToolBar n’a pas le style [**TBSTYLE \_ ex \_ Column**](toolbar-extended-styles.md) , ce message n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

