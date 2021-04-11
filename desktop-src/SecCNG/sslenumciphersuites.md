---
description: Énumère les suites de chiffrement prises en charge par un fournisseur de protocole de protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: SslEnumCipherSuites, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318993"
---
# <a name="sslenumciphersuites-function"></a>SslEnumCipherSuites fonction)

La fonction **SslEnumCipherSuites** énumère les suites de chiffrement prises en charge par un fournisseur de protocole de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*hPrivateKey* \[ dans, facultatif\]
</dt> <dd>

Handle d’une [*clé privée*](/windows/desktop/SecGloss/p-gly). Lorsqu’une clé privée est spécifiée, **SslEnumCipherSuites** énumère les suites de chiffrement qui sont compatibles avec la clé privée. Par exemple, si la clé privée est une clé DSS, seules les suites de \_ chiffrement DSS dhe sont retournées. Si la clé privée est une clé RSA, mais ne prend pas en charge les opérations de déchiffrement brut, les suites de chiffrement SSL2 ne sont pas retournées.

Affectez la valeur **null** à ce paramètre lorsque vous ne spécifiez pas de clé privée.

> [!Note]  
> Un descripteur *hPrivateKey* est obtenu en appelant la fonction [**SslOpenPrivateKey**](sslopenprivatekey.md) . Les handles obtenus à partir de la fonction [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) ne sont pas pris en charge.

 

</dd> <dt>

*ppCipherSuite* \[ à\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ \_ suite de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) pour recevoir l’adresse de la suite de chiffrement suivante dans la liste.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Pointeur vers une mémoire tampon qui indique la position actuelle dans la liste de suites de chiffrement.

Affectez au pointeur la **valeur null** lors du premier appel à **SslEnumCipherSuites**. À chaque appel suivant, repassez la valeur non modifiée à **SslEnumCipherSuites**.

Lorsqu’il n’y a plus de suites de chiffrement disponibles, vous devez libérer *ppEnumState* en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>      | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/>                     |
| <dl> <dt>**NPD \_ AUCUN \_ autre \_ élément**</dt> <dt>0x8009002AL</dt> </dl> | Aucune suite de chiffrement supplémentaire n’est prise en charge.<br/>                    |



 

## <a name="remarks"></a>Notes

Pour énumérer toutes les suites de chiffrement prises en charge par le fournisseur SSL, appelez la fonction **SslEnumCipherSuites** dans une boucle jusqu’à **NPD, \_ aucun \_ autre \_ élément** n’est retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Ncrypt. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_suite de \_ chiffrement SSL NCRYPT \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

