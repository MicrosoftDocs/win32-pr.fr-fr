---
title: Message EM_GETIMEMODEBIAS (RichEdit. h)
description: Récupère le décalage de mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033056"
---
# <a name="em_getimemodebias-message"></a>\_Message GETIMEMODEBIAS em

Récupère le décalage de mode de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit Microsoft.

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

Ce message retourne le paramètre de décalage en mode IME actuel.

## <a name="remarks"></a>Notes

Pour récupérer le décalage en mode Text Services Framework, utilisez [**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md).

L’application doit appeler [**em \_ ISIME**](em-isime.md) avant d’appeler cette fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_GETCTFMODEBIAS em**](em-getctfmodebias.md)
</dt> </dl>

 

 





