---
title: Message EM_GETIMEOPTIONS (RichEdit. h)
description: Récupère les options de l’éditeur de méthode d’entrée (IME) en cours.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS les contrôles de message Windows
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
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104821"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETIMEOPTIONS em**](em-setimeoptions.md)
</dt> </dl>

 

 





