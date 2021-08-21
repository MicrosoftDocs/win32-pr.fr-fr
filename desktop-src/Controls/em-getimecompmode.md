---
title: Message EM_GETIMECOMPMODE (RichEdit. h)
description: Récupère le mode IME (éditeur de méthode d’entrée) actuel pour un contrôle RichEdit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019547"
---
# <a name="em_getimecompmode-message"></a>\_Message GETIMECOMPMODE em

Récupère le mode IME (éditeur de méthode d’entrée) actuel pour un contrôle RichEdit.

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

La valeur de retour est l’une des valeurs suivantes.



| Code de retour                                                                                     | Description                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_ NOTOPEN**</dt> </dl>     | L’IME n’est pas ouvert.<br/>  |
| <dl> <dt>**ICM \_ LEVEL3**</dt> </dl>      | Mode inline réel.<br/> |
| <dl> <dt>**ICM \_ D’ISOLEMENT2**</dt> </dl>      | Niveau 2.<br/>          |
| <dl> <dt>**ICM \_ D’ISOLEMENT2 \_ 5**</dt> </dl>   | Niveau 2,5<br/>         |
| <dl> <dt>**ICM \_ SUI du D’ISOLEMENT2 \_**</dt> </dl> | Interface utilisateur spéciale.<br/>       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





