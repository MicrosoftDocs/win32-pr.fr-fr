---
description: Libère une structure de contexte de signataire \_ allouée par un appel précédent à la fonction SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerContext fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526155"
---
# <a name="signerfreesignercontext-function"></a>SignerFreeSignerContext fonction)

La fonction **SignerFreeSignerContext** libère une structure de [**\_ contexte de signataire**](signer-context.md) allouée par un appel précédent à la fonction [**SignerSignEx**](signersignex.md) .

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSignerContext* \[ dans\]
</dt> <dd>

Pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**contexte du signataire \_**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
