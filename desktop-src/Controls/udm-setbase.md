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
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115438"
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

## <a name="return-value"></a>Valeur de retour

La valeur de retour est la valeur de base précédente. Si une base non valide est spécifiée, la valeur de retour est zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





