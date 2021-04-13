---
title: Message EM_GETIMECOMPMODE (RichEdit. h)
description: Récupère le mode IME (éditeur de méthode d’entrée) actuel pour un contrôle RichEdit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE les contrôles de message Windows
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
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466106"
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
| <dl> <dt>**\_NOTOPEN ICM**</dt> </dl>     | L’IME n’est pas ouvert.<br/>  |
| <dl> <dt>**\_NIVEAU3 ICM**</dt> </dl>      | Mode inline réel.<br/> |
| <dl> <dt>**Le \_ d’isolement2**</dt> </dl>      | Niveau 2.<br/>          |
| <dl> <dt>**ICM- \_ d’isolement2 \_ 5**</dt> </dl>   | Niveau 2,5<br/>         |
| <dl> <dt>**CCI \_ d’isolement2- \_ sui**</dt> </dl> | Interface utilisateur spéciale.<br/>       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





