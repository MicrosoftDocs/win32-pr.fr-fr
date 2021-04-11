---
title: Message EM_GETOLEINTERFACE (RichEdit. h)
description: Récupère un objet IRichEditOle qu’un client peut utiliser pour accéder à la fonctionnalité COM (Component Object Model) d’un contrôle RichEdit.
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104818"
---
# <a name="em_getoleinterface-message"></a>\_Message GETOLEINTERFACE em

Récupère un objet [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) qu’un client peut utiliser pour accéder à la fonctionnalité com (Component Object Model) d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un pointeur qui reçoit l’objet [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) . Le contrôle appelle la méthode [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) pour l’objet avant de retourner, de sorte que l’application appelante doit appeler la méthode [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) lorsque l’objet est terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 

