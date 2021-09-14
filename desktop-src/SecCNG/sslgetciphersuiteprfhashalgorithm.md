---
description: 'Retourne l’identificateur d’algorithme CNG (Cryptography API : Next Generation) de l’algorithme de hachage utilisé pour la fonction Pseudo-aléatoire (PRF) TLS (Transport Layer Security Protocol) pour le protocole d’entrée, la suite de chiffrement et le type de clé.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: SslGetCipherSuitePRFHashAlgorithm, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218108"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>SslGetCipherSuitePRFHashAlgorithm fonction)

La fonction **SslGetCipherSuitePRFHashAlgorithm** retourne l’identificateur d’ALGORITHMe CNG (Cryptography API : Next Generation) de l' [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) utilisé pour la [*fonction Pseudo-aléatoire*](/windows/desktop/SecGloss/p-gly) (PRF) TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) pour le protocole d’entrée, la suite de chiffrement et le type de clé.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

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

L’une des valeurs d' [**identificateur de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Pour les types de clés qui ne sont pas du [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC), définissez ce paramètre sur zéro.

</dd> <dt>

*szPRFHash* \[ à\]
</dt> <dd>

Un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) pour le hachage qui sera utilisé pour le PRF TLS.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.<br/>                |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *szPRFHash* a la valeur **null**.<br/>                                     |
| <dl> <dt>**NPD \_ 0x80090029L non \_ pris en charge**</dt> <dt></dt> </dl>     | La fonction sélectionnée n’est pas prise en charge dans la version spécifiée de l’interface.<br/> |
| <dl> <dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt> </dl>         | Le paramètre *dwFlags* doit avoir la valeur zéro.<br/>                                      |



 

## <a name="remarks"></a>Notes

Cette fonction **SslGetCipherSuitePRFHashAlgorithm** est appelée pour les conversations TLS 1,2 ou ultérieures pour interroger l’algorithme de hachage qui sera utilisé dans le PRF TLS.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

