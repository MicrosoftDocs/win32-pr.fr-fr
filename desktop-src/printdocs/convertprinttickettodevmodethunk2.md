---
description: Convertit un ticket d’impression en une structure DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: cf05ab6739dad09332ebc6746a05f3c40ef32de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118034"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2 fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions ultérieures de Windows. [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Convertit un ticket d’impression en une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* \[ dans\]
</dt> <dd>

Handle d’un fournisseur de tickets d’impression ouvert. Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pPrintTicket* \[ dans\]
</dt> <dd>

Mémoire tampon qui contient le ticket d’impression à convertir.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon passée dans *pPrintTicket*.

</dd> <dt>

*BaseType* \[ dans\]
</dt> <dd>

Valeur indiquant si le [**DEVMODE par défaut**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de l’utilisateur ou le **DEVMODE** par défaut de la file d’attente à l’impression est utilisé pour fournir des valeurs au **DEVMODE** de sortie lorsque *pPrintTicket* ne spécifie pas tous les paramètres possibles pour un **DEVMODE**. La valeur de ce paramètre doit être un membre de l’énumération [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , castée en **int**.

</dd> <dt>

*étendue* \[ dans\]
</dt> <dd>

Valeur qui spécifie la portée de *pPrintTicket*. Cette valeur peut spécifier une page unique, un document entier ou tous les documents du travail d’impression. La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.

</dd> <dt>

*ppDevmode* \[ à\]
</dt> <dd>

Adresse de la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)nouvellement créée. Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon. Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbDevModeLength* \[ à\]
</dt> <dd>

Taille, en octets, du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retourné dans *ppDevmode*.

</dd> <dt>

 le \[ out, facultatif\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide concernant le ticket d’impression dans *pPrintTicket*. S’il est valide, la **valeur est null**. Si *l'* appel de la fonction n’est pas **null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

