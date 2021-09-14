---
description: Déchiffre un paquet SSL (Single SSL (Secure Sockets Layer) Protocol).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: SslDecryptPacket, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013633"
---
# <a name="ssldecryptpacket-function"></a>SslDecryptPacket fonction)

la fonction **SslDecryptPacket** déchiffre un paquet SSL (Single [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*HKEY* \[ in, out\]
</dt> <dd>

Handle de la clé utilisée pour déchiffrer le paquet.

</dd> <dt>

*pbInput* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon qui contient le paquet à déchiffrer.

</dd> <dt>

*cbInput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbInput* .

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à contenir le paquet déchiffré.

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Nombre d’octets écrits dans la mémoire tampon *pbOutput* .

</dd> <dt>

 N \[ dans\]
</dt> <dd>

Numéro de séquence qui correspond à ce paquet.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

La longueur du paquet peut être égale à zéro, par exemple lors du déchiffrement d’un message « HelloRequest ».

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

