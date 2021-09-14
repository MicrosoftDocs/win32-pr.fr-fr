---
title: Message EM_SETOLECALLBACK (RichEdit. h)
description: Fournit un contrôle Rich Edit à un objet IRichEditOleCallback que le contrôle utilise pour obtenir des ressources et des informations liées à OLE à partir du client.
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006381"
---
# <a name="em_setolecallback-message"></a>\_Message SETOLECALLBACK em

Fournit un contrôle Rich Edit à un objet [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) que le contrôle utilise pour obtenir des ressources et des informations liées à OLE à partir du client.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un objet [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) . Le contrôle appelle la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour l’objet avant de retourner.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

