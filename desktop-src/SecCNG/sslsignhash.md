---
description: Signe un hachage à l’aide de la clé privée spécifiée.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: SslSignHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218009"
---
# <a name="sslsignhash-function"></a>SslSignHash fonction)

La fonction **SslSignHash** signe un [*hachage*](/windows/desktop/SecGloss/h-gly) à l’aide de la [*clé privée*](/windows/desktop/SecGloss/p-gly)spécifiée. Le processus de signature est exécuté sur le serveur.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hPrivateKey* \[ dans\]
</dt> <dd>

Handle de la clé privée à utiliser pour signer le hachage.

</dd> <dt>

*pbHashValue* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le hachage à signer.

</dd> <dt>

*cbHashValue* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbHashValue* .

</dd> <dt>

*pbSignature* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit la signature du hachage. Le paramètre *cbSignature* contient la taille de cette mémoire tampon. Pour déterminer la taille de mémoire tampon requise, affectez la valeur **null** au paramètre *pbSignature* . La taille requise de la mémoire tampon est retournée dans le paramètre *pcbResult* .

</dd> <dt>

*cbSignature* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbSignature* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui, une fois terminée, contient le nombre réel d’octets écrits dans la mémoire tampon *pbSignature* .

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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

