---
description: Appelé par le compilateur pour implémenter des extensions de gestion structurée des exceptions.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Fonction __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017827"
---
# <a name="__c_specific_handler-function"></a>\_\_\_Fonction de gestionnaire spécifique à C \_

Appelé par le compilateur pour implémenter des extensions de gestion structurée des exceptions.

L’adresse relative du gestionnaire spécifique au langage est présente dans les informations de déroulement \_ chaque fois que Flags UNW Flag \_ \_ EHANDLER ou UNW \_ Flag \_ UHANDLER sont définis. Le gestionnaire spécifique au langage est appelé dans le cadre de la recherche d’un gestionnaire d’exceptions ou dans le cadre d’un déroulement. Pour plus d’informations, consultez [gestionnaire spécifique](/cpp/build/language-specific-handler)à une langue.

## <a name="syntax"></a>Syntaxe


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ExceptionRecord* \[ dans\]
</dt> <dd>

Fournit un pointeur vers un enregistrement d’exception, qui a la définition Win64 standard.

</dd> <dt>

*EstablisherFrame* \[ dans\]
</dt> <dd>

Adresse de la base de l’allocation de pile fixe pour cette fonction.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Pointe vers le contexte d’exception au moment où l’exception a été levée (dans le cas du gestionnaire d’exceptions) ou dans le contexte de « déroulement » actuel (dans le cas du gestionnaire de terminaisons).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Pointe vers le contexte du répartiteur pour cette fonction.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Bibliothèque<br/> | <dl> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

