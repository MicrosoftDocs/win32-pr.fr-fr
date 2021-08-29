---
title: TLSGetServerCertificate fonction)
description: Retourne le certificat du serveur de licences Bureau à distance.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSGetServerCertificate
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f32b939eff90a5043b1fc29d90534d2d51215522f1f5ff07ba45e817014936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986939"
---
# <a name="tlsgetservercertificate-function"></a>TLSGetServerCertificate fonction)

Retourne le certificat du serveur de licences Bureau à distance.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hHandle* \[ dans\]
</dt> <dd>

Handle vers un serveur de licences Bureau à distance qui est ouvert par un appel à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .

</dd> <dt>

*bSignCert* \[ dans\]
</dt> <dd>

**True** si le certificat de signature est **false** dans le cas d’un certificat Exchange.

</dd> <dt>

*ppbCertBlob* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un pointeur vers une mémoire tampon qui contient le certificat.

</dd> <dt>

*lpdwCertBlobLen* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille du certificat retourné.

</dd> <dt>

*pdwErrCode* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le code d’erreur.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)


</dt> <dd>

L’appel a réussi.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>Protocole **TLS \_ \_SELFSIGN \_ certificat W** (4007)


</dt> <dd>

Le certificat retourné est un certificat auto-signé.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>Protocole **TLS \_ \_Certificat Temp \_ SELFSIGN \_** (4009)


</dt> <dd>

Le certificat retourné est temporaire.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>Protocole **TLS \_ \_Accès E \_ refusé** (5003)


</dt> <dd>

Accès refusé.

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>Protocole **TLS \_ E \_ allouer un \_ descripteur** (5007)


</dt> <dd>

Le serveur est trop occupé pour traiter la demande.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>Protocole **TLS \_ E \_ aucun \_ certificat** (5022)


</dt> <dd>

Impossible de récupérer un certificat.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne les valeurs de retour possibles suivantes.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

L’appel a réussi. Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.

</dd> <dt>

**\_argument RPC \_ non valide \_**
</dt> <dd>

L'argument n'était pas valide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

