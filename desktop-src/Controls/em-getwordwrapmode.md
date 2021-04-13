---
title: Message EM_GETWORDWRAPMODE (RichEdit. h)
description: Obtient le retour automatique à la ligne et les options de saut de mot en cours pour le contrôle RichEdit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464542"
---
# <a name="em_getwordwrapmode-message"></a>\_Message GETWORDWRAPMODE em

Obtient le retour automatique à la ligne et les options de saut de mot en cours pour le contrôle RichEdit.

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.

 

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

Le message retourne les options retour automatique à la ligne et saut de mot en cours.

## <a name="remarks"></a>Notes

Ce message ne doit pas être envoyé par la procédure de césure définie par l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





