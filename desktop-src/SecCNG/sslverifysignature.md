---
description: Vérifie la signature spécifiée à l’aide du hachage et de la clé publique fournis.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: SslVerifySignature, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905658"
---
# <a name="sslverifysignature-function"></a>SslVerifySignature fonction)

La fonction **SslVerifySignature** vérifie la signature spécifiée à l’aide du [*hachage*](/windows/desktop/SecGloss/h-gly) fourni et de la [*clé publique*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPublicKey* \[ dans\]
</dt> <dd>

Handle de la clé publique.

</dd> <dt>

*pbHashValue* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le hachage à utiliser pour vérifier la signature.

</dd> <dt>

*cbHashValue* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbHashValue* .

</dd> <dt>

*pbSignature* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la signature à vérifier.

</dd> <dt>

*cbSignature* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbSignature* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="remarks"></a>Remarques

La fonction **SslVerifySignature** n’est pas appelée actuellement par Windows. Cette fonction est une partie obligatoire de l’interface du fournisseur SSL et doit être entièrement implémentée pour garantir la compatibilité ascendante.

Les implémentations actuelles du côté serveur de la connexion TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) appellent la fonction [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) lors de l’authentification du client pour traiter le message de vérification du certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

