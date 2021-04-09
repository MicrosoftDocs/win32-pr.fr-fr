---
title: Message EM_SETSTORYTYPE (RichEdit. h)
description: Définit le type d’histoire.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843362"
---
# <a name="em_setstorytype-message"></a>\_Message SETSTORYTYPE em

Définit le type d’histoire.


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’histoire.

</dd> <dt>

*lParam* 
</dt> <dd>

Type du nouveau récit. Pour obtenir la liste des types de récits, consultez [**em \_ GETSTORYTYPE**](em-getstorytype.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type d’histoire qui a été défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





