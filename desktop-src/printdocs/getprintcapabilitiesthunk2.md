---
description: Récupère les fonctionnalités d’imprimantes mises en forme en conformité avec le schéma d’impression XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: eb60f1cdabad6287e236fc099fc304e9e7de83ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523236"
---
# <a name="getprintcapabilitiesthunk2-function"></a>GetPrintCapabilitiesThunk2 fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows. [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Récupère les fonctionnalités de l’imprimante mises en forme en conformité avec le [schéma d’impression](./printschema.md)XML.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
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

Mémoire tampon qui contient les données du ticket d’impression, exprimées en XML, comme décrit dans le [schéma d’impression](./printschema.md).

</dd> <dt>

*cbPrintTicket* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par *pPrintTicket*.

</dd> <dt>

*ppbPrintCapabilities* \[ à\]
</dt> <dd>

L’adresse de la mémoire tampon allouée par cette fonction et contient les informations de fonctionnalités d’impression valides, encodées au format XML. Cette fonction appelle [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) pour allouer cette mémoire tampon. Lorsque la mémoire tampon n’est plus nécessaire, l’appelant doit la libérer en appelant [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintCapabilitiesLength* \[ à\]
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par *ppbPrintCapabilities*.

</dd> <dt>

*pbstrErrorMessage* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une chaîne qui spécifie ce qui, le cas échéant, n’est pas valide sur *pPrintTicket*. S’il est valide, cette valeur est **null**. Si *pbstrErrorMessage* n’a pas la **valeur null** lorsque la fonction retourne, l’appelant doit libérer la chaîne avec [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

