---
title: TLSLicenseEnumEnd fonction)
description: Continue à partir d’un appel précédent à la fonction TLSLicenseEnumBegin et met fin à l’énumération.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSLicenseEnumEnd
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193420"
---
# <a name="tlslicenseenumend-function"></a>TLSLicenseEnumEnd fonction)

Continue à partir d’un appel précédent à la fonction [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) et met fin à l’énumération.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hHandle* \[ dans\]
</dt> <dd>

Handle vers un serveur de licences Bureau à distance. Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*pdwErrCode* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)


</dt> <dd>

L’appel a réussi.

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**Lserver \_ \_ \_ Pointeur E non valide** (5005)


</dt> <dd>

Le descripteur n’est pas valide.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette fonction retourne les valeurs de retour possibles suivantes.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

L’appel a réussi. Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.

</dd> <dt>

**\_argument RPC \_ non valide \_**
</dt> <dd>

L’argument n’est pas valide.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> </dl>

 

