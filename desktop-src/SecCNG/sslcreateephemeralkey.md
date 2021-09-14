---
description: Crée une clé éphémère à utiliser pendant l’authentification qui se produit au cours de la négociation SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: SslCreateEphemeralKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013638"
---
# <a name="sslcreateephemeralkey-function"></a>SslCreateEphemeralKey fonction)

La fonction **SslCreateEphemeralKey** crée une clé éphémère à utiliser pendant l’authentification qui se produit pendant la négociation SSL ( [*protocole SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*phEphemeralKey* \[ à\]
</dt> <dd>

Handle de la clé éphémère.

</dd> <dt>

*dwProtocol* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ dans\]
</dt> <dd>

L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Affectez la valeur zéro à ce paramètre pour les types de clés qui ne sont pas du [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC).

</dd> <dt>

*dwKeyBitLen* \[ dans\]
</dt> <dd>

Longueur, en bits, de la clé.

</dd> <dt>

*pbParams* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les paramètres de la clé qui doit être créée. Si une suite de chiffrement d’algorithme d’échange de clés (dhe) [*Diffie-Hellman (éphémère)*](/windows/desktop/SecGloss/d-gly) n’est pas utilisée, affectez la valeur **null** au paramètre *pbParams* et le paramètre *cbParams* à zéro.

</dd> <dt>

*cbParams* \[ dans\]
</dt> <dd>

Longueur, en octets, des données dans la mémoire tampon *pbParams* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.



| Code/valeur de retour                                                                                                                                                       | Description                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire est insuffisante pour allouer la mémoire tampon.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le descripteur *hSslProvider* n’est pas valide.<br/>              |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | L’un des paramètres fournis n’est pas valide.<br/>         |



 

## <a name="remarks"></a>Notes

Lors de l’utilisation d’une suite de chiffrement DHE, l’implémentation SSL interne transmet les paramètres Server *p* et *g* à la fonction **SslCreateEphemeralKey** dans les paramètres *pbParams* et *cbParams* .

Le format des données dans la mémoire tampon *pbParams* est le même que celui utilisé lors de la définition de la propriété de [**\_ \_ paramètres bcrypt DH**](cng-property-identifiers.md) , et il commence par une structure d' [**\_ \_ \_ en-tête de paramètre bcrypt DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

