---
title: Énumération BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: L’énumération BG_ERROR_CONTEXT définit les valeurs constantes qui spécifient le contexte dans lequel l’erreur s’est produite.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Énumération BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915671"
---
# <a name="bg_error_context-enumeration"></a>Énumération BG_ERROR_CONTEXT

L’énumération **BG_ERROR_CONTEXT** définit les valeurs constantes qui spécifient le contexte dans lequel l’erreur s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**
</dt> <dd>

Aucune erreur ne s’est produite.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**
</dt> <dd>

L’erreur est liée au fichier distant spécifié. Par exemple, l’URL n’était pas accessible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**
</dt> <dd>

Non pris en charge.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





