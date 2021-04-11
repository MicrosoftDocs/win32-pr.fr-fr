---
description: Ouvre une instance d’un fournisseur de tickets d’impression.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: BindPTProviderThunk fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202702"
---
# <a name="bindptproviderthunk-function"></a>BindPTProviderThunk fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Ouvre une instance d’un fournisseur de tickets d’impression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszPrinterName* \[ dans\]
</dt> <dd>

Nom complet d’une file d’attente à l’impression.

</dd> <dt>

*MaxVersion* \[ dans\]
</dt> <dd>

La dernière version du [schéma d’impression](./printschema.md) que l’appelant prend en charge.

</dd> <dt>

*prefVersion* \[ dans\]
</dt> <dd>

Version du schéma d' [impression](./printschema.md) demandé par l’appelant.

</dd> <dt>

*phProvider* \[ à\]
</dt> <dd>

Pointeur vers un handle du fournisseur de tickets d’impression.

</dd> <dt>

*usedVersion* \[ à\]
</dt> <dd>

Version du schéma d' [impression](./printschema.md) que le fournisseur de tickets d’impression utilisera.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Notes

Avant d’appeler cette fonction, le thread appelant doit initialiser COM en appelant [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

