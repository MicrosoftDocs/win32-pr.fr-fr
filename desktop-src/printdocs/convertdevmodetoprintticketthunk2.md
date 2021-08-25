---
description: Convertit une structure DEVMODE en un ticket d’impression.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950389"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2 fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions ultérieures de Windows. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Convertit une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en un ticket d’impression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* \[ dans\]
</dt> <dd>

Handle d’un fournisseur de tickets d’impression ouvert. Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pDevmode* \[ dans\]
</dt> <dd>

Pointeur vers le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) à convertir.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Taille, en octets, du [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passé dans *pDevmode*.

</dd> <dt>

*étendue* \[ dans\]
</dt> <dd>

Valeur qui spécifie la portée de *ppPrintTicket*. Cette valeur peut spécifier une page unique, un document entier ou tous les documents du travail d’impression. La valeur de ce paramètre doit être un membre de l’énumération [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , castée en tant que valeur **DWORD**.

</dd> <dt>

*ppPrintTicket* \[ à\]
</dt> <dd>

Adresse de la mémoire tampon qui contient un ticket d’impression qui représente le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passé dans *pDevmode*. Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon. Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintTicketLength* \[ à\]
</dt> <dd>

Taille, en octets, du ticket d’impression retourné dans *ppPrintTicket*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

