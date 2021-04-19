---
description: Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545858"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2 fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows. [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Fusionne deux tickets d’impression et retourne un ticket d’impression valide et viable.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* \[ dans\]
</dt> <dd>

Handle d’un fournisseur de tickets d’impression ouvert. Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pBasePrintTicket* \[ dans\]
</dt> <dd>

Mémoire tampon qui contient les données de ticket d’impression de base, exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md).

</dd> <dt>

*basePrintTicketLength* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par *pBasePrintTicket*.

</dd> <dt>

*pDeltaPrintTicket* \[ dans, facultatif\]
</dt> <dd>

Mémoire tampon qui contient le ticket d’impression à fusionner. Les données du ticket d’impression sont exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md). La valeur de ce paramètre peut être **null**.

</dd> <dt>

*deltaPrintTicketLength* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par *pDeltaPrintTicket*.

</dd> <dt>

*étendue* \[ dans\]
</dt> <dd>

Valeur qui spécifie si l’étendue de *pDeltaPrintTicket* et *ppValidatedPrintTicket* est une page unique, un document entier ou tous les documents du travail d’impression. La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.

</dd> <dt>

*ppValidatedPrintTicket* \[ à\]
</dt> <dd>

Adresse de la mémoire tampon qui contient les tickets d’impression fusionnés et validés. Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon. Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pValidatedPrintTicketLength* \[ à\]
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par *ppValidatedPrintTicket*.

</dd> <dt>

*pbstrErrorMessage* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide concernant le ticket d’impression dans *pBasePrintTicket* ou *pDeltaPrintTicket*. Si elles sont toutes deux valides, cette valeur est **null**. Si *pbstrErrorMessage* n’a pas la **valeur null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

