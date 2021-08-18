---
description: Retourne un handle pour le hachage de négociation.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: SslHashHandshake, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906097"
---
# <a name="sslhashhandshake-function"></a>SslHashHandshake fonction)

La fonction **SslHashHandshake** retourne un handle vers le hachage de négociation.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hHandshakeHash* \[ in, out\]
</dt> <dd>

Handle de l’objet de hachage.

</dd> <dt>

*pbInput* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui contient les données à hacher.

</dd> <dt>

*cbInput* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbInput* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

## <a name="remarks"></a>Remarques

La fonction **SslHashHandshake** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.

1.  La fonction [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) est appelée pour obtenir un handle de hachage.
2.  La fonction **SslHashHandshake** est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.
3.  La fonction [**SslComputeFinishedHash**](sslcomputefinishedhash.md) est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

