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
ms.openlocfilehash: 9a7b16494bf0e34606809d5b4670a05d4ae3c60a6ea49c8103688c6e09676c98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048299"
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

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

