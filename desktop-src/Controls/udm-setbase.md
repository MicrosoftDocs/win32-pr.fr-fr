---
title: Message UDM_SETBASE (commctrl. h)
description: Définit la base de base pour un contrôle up-up. La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux. Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f9fd3750a70e676c3e9f32efe9ff0bfd9b300b812d09f4a04c34e4a90f36933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669077"
---
# <a name="udm_setbase-message"></a>\_Message SETBASE UDM

Définit la base de base pour un contrôle up-up. La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux. Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nouvelle valeur de base pour le contrôle. Ce paramètre peut avoir la valeur 10 pour Decimal ou 16 pour hexadécimal.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la valeur de base précédente. Si une base non valide est spécifiée, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





