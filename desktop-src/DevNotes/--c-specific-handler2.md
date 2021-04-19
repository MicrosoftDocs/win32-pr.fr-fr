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
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542298"
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



 

