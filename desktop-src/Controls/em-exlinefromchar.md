---
title: Message EM_EXLINEFROMCHAR (RichEdit. h)
description: Détermine la ligne qui contient le caractère spécifié dans un contrôle RichEdit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007659"
---
# <a name="em_exlinefromchar-message"></a>\_Message EXLINEFROMCHAR em

Détermine la ligne qui contient le caractère spécifié dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Index de base zéro du caractère.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message retourne l’index de base zéro de la ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





