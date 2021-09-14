---
description: Retourne une \_ \_ \_ structure de longueurs de chiffrement SSL NCRYPT qui contient les longueurs d’en-tête et de code de fin du protocole d’entrée, de la suite de chiffrement et du type de clé.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: SslLookupCipherLengths, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218025"
---
# <a name="ssllookupcipherlengths-function"></a>SslLookupCipherLengths fonction)

La fonction **SslLookupCipherLengths** retourne une structure de [**\_ \_ \_ longueurs de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) qui contient les longueurs d’en-tête et de code de fin du protocole d’entrée, de la suite de chiffrement et du type de clé.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
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

*pCipherLengths* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à recevoir la structure des [**\_ \_ \_ longueurs de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .

</dd> <dt>

*cbCipherLengths* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pCipherLengths* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.<br/>                                                      |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *pCipherLengths* a la valeur **null** ou la longueur de la mémoire tampon spécifiée par le *cbCipherLengths* est trop petite.<br/> |
| <dl> <dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt> </dl>         | Le paramètre *dwFlags* doit avoir la valeur zéro.<br/>                                                                            |



 

## <a name="remarks"></a>Notes

La fonction **SslLookupCipherLengths** est appelée pour les conversations TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,1 ou ultérieures pour interroger les longueurs d’en-tête et de code de fin pour le protocole, la suite de chiffrement et le type de clé demandés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

