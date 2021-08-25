---
title: Message EM_GETIMEOPTIONS (RichEdit. h)
description: Récupère les options de l’éditeur de méthode d’entrée (IME) en cours.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049059"
---
# <a name="em_getimeoptions-message"></a>\_Message GETIMEOPTIONS em

Récupère les options de l’éditeur de méthode d’entrée (IME) en cours.

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

Ce message retourne une ou plusieurs des valeurs d’indicateur d’option IME décrites dans le message [**em \_ SETIMEOPTIONS**](em-setimeoptions.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETIMEOPTIONS em**](em-setimeoptions.md)
</dt> </dl>

 

 





