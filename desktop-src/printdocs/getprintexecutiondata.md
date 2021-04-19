---
description: Le GetPrintExecutionData récupère le contexte d’impression actuel.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: GetPrintExecutionData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542007"
---
# <a name="getprintexecutiondata-function"></a>GetPrintExecutionData fonction)

Le **GetPrintExecutionData** récupère le contexte d’impression actuel.

> [!Note]  
> Cette fonction est destinée à être utilisée par les pilotes d’imprimante qui s’exécutent dans le contexte du spouleur d’impression.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’adresse de la structure [**de \_ \_ données d’exécution**](print-execution-data.md) de l’impression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la fonction est réussie ; Sinon, **false**. Si la valeur de retour est **false**, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir l’état d’erreur.

## <a name="remarks"></a>Notes

Les pilotes d’imprimante doivent appeler [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) sur le module winspool. drv pour récupérer l’adresse de la fonction **GetPrintExecutionData** , car **GetPrintExecutionData** n’est pas pris en charge sur Windows Vista ou les versions antérieures de Windows.

**GetPrintExecutionData** échoue uniquement si la valeur de *pData* est **null**.

La valeur du membre **clientAppPID** des [**données d' \_ exécution \_**](print-execution-data.md) de l’impression n’est significative que si la valeur de **Context** est le **contexte d’exécution d’impression \_ \_ \_ WOW64**. Si la valeur du **contexte** n’affiche pas le **\_ contexte d’exécution \_ \_ WOW64**, la valeur de **clientAppPID** est 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**Imprimer \_ le \_ contexte d’exécution**](print-execution-context.md)
</dt> <dt>

[**Imprimer \_ les \_ données d’exécution**](print-execution-data.md)
</dt> </dl>

 

