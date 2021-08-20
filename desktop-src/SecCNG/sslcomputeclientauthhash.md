---
description: Calcule un hachage à utiliser pendant l’authentification par certificat.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: SslComputeClientAuthHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 59d1a4d8491175acb0f833cbafb430faae9b36b38a179970b7a99d6b0077591d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907160"
---
# <a name="sslcomputeclientauthhash-function"></a>SslComputeClientAuthHash fonction)

La fonction **SslComputeClientAuthHash** calcule un [*hachage*](/windows/desktop/SecGloss/h-gly) à utiliser pendant l’authentification par [*certificat*](/windows/desktop/SecGloss/c-gly) .

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
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

*hMasterKey* \[ dans\]
</dt> <dd>

Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*hHandshakeHash* \[ dans\]
</dt> <dd>

Handle du hachage du protocole de transfert calculé jusqu’à présent.

</dd> <dt>

*pszAlgId* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui identifie l' [*algorithme de chiffrement*](/windows/desktop/SecGloss/c-gly)demandé. Il peut s’agir de l’un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) standard ou de l’identificateur d’un autre algorithme inscrit.

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly). Le paramètre *cbOutput* contient la taille de cette mémoire tampon. Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui spécifie la longueur, en octets, du hachage écrit dans la mémoire tampon *pbOutput* .

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

La fonction **SslComputeClientAuthHash** calcule le hachage qui est envoyé dans le message de vérification du certificat de la négociation SSL. La valeur de hachage est calculée en créant un hachage qui contient le secret principal avec un hachage de tous les messages de négociation précédents envoyés ou reçus. Pour plus d’informations sur la séquence de négociation SSL, consultez [Description du protocole de transfert de SSL (Secure Sockets Layer) (SSL)](https://support.microsoft.com/kb/257591).

La manière dont le hachage est calculé dépend du protocole et de la suite de chiffrement utilisés. En outre, le hachage dépend du type de clé d’authentification du client utilisé ; le paramètre *pszAlgId* indique le type de clé utilisé pour l’authentification du client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

