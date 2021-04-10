---
description: Calcule le hachage envoyé dans le message terminé de la négociation SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: SslComputeFinishedHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951681"
---
# <a name="sslcomputefinishedhash-function"></a>SslComputeFinishedHash fonction)

La fonction **SslComputeFinishedHash** calcule le [*hachage*](/windows/desktop/SecGloss/h-gly) envoyé dans le message terminé de la négociation du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL). Pour plus d’informations sur la séquence de négociation SSL, consultez [Description du protocole de transfert de SSL (Secure Sockets Layer) (SSL)](https://support.microsoft.com/kb/257591).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*hMasterKey* \[ dans\]
</dt> <dd>

Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ dans\]
</dt> <dd>

Handle du hachage des messages de négociation.

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le hachage pour le message de fin.

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Une des constantes suivantes.



| Valeur                                                                                                                                                                                                                                                      | Signification                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Indicateur client SSL**</dt> <dt>0x00000001</dt> </dl> | Spécifie qu’il s’agit d’un appel client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Indicateur de serveur SSL**</dt> <dt>0x00000002</dt> </dl> | Spécifie qu’il s’agit d’un appel de serveur.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.



| Code/valeur de retour                                                                                                                                                                | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_HANDLE 2148073510 non valide**</dt> <dt>(0x80090026)</dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

La fonction **SslComputeFinishedHash** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.

1.  La fonction [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) est appelée pour obtenir un handle de hachage.
2.  La fonction [**SslHashHandshake**](sslhashhandshake.md) est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.
3.  La fonction **SslComputeFinishedHash** est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.

La valeur de hachage est calculée en hachant le secret principal avec un hachage de tous les messages de négociation précédents envoyés ou reçus.

La valeur de *cbOutput* détermine la longueur des données de hachage. Lorsque le protocole TLS ( [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) ) 1,0 est utilisé, il doit toujours être de 12 (octets). Pour plus d’informations, consultez [la Version 1,0 du protocole TLS](https://www.ietf.org/rfc/rfc2246.txt).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

