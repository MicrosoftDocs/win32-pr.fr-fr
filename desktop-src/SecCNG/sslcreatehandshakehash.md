---
description: Obtient un handle de hachage utilisé pour hacher les messages de négociation.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: SslCreateHandshakeHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013636"
---
# <a name="sslcreatehandshakehash-function"></a>SslCreateHandshakeHash fonction)

La fonction **SslCreateHandshakeHash** obtient un descripteur de hachage utilisé pour hacher les messages de négociation.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ à\]
</dt> <dd>

Handle de hachage qui peut être passé à d’autres fonctions du fournisseur SSL.

</dd> <dt>

*dwProtocol* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

> [!Note]  
> Cette fonction n’est pas utilisée avec le protocole SSL 2,0.

 

</dd> <dt>

*dwCipherSuite* \[ dans\]
</dt> <dd>

L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire est insuffisante pour allouer la mémoire tampon de hachage.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le descripteur *hSslProvider* n’est pas valide.<br/>                   |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | *PhHandshakeHash* a la valeur null.<br/>                            |



 

## <a name="remarks"></a>Notes

La fonction **SslCreateHandshakeHash** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.

1.  La fonction **SslCreateHandshakeHash** est appelée pour obtenir un handle de hachage.
2.  La fonction [**SslHashHandshake**](sslhashhandshake.md) est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.
3.  La fonction [**SslComputeFinishedHash**](sslcomputefinishedhash.md) est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

