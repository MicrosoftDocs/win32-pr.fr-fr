---
description: Importe une clé dans le fournisseur de protocole du protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: SslImportKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 00dbe668c28e234c0ed4fdc7950b6b9627ae5aaba46bbef4e17d1eb8cb213f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906087"
---
# <a name="sslimportkey-function"></a>SslImportKey fonction)

La fonction **SslImportKey** importe une clé dans le fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*phKey* \[ à\]
</dt> <dd>

Pointeur vers le handle de la [*clé de chiffrement*](/windows/desktop/SecGloss/c-gly) pour recevoir la clé importée.

</dd> <dt>

*pszBlobType* \[ dans\]
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui contient un identificateur spécifiant le type d' [*objet BLOB*](/windows/desktop/SecGloss/b-gly) contenu dans la mémoire tampon *pbInput* . Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ objet BLOB public de BCRYPT DH \_**</dt> </dl>    | Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ \_ objet blob de clé**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) de la clé de données BCRYPT immédiatement suivie des données de clé.<br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_objet BLOB ECCPUBLIC de BCRYPT \_**</dt> </dl>     | Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)ECC ( [*Elliptic Curve Cryptography*](/windows/desktop/SecGloss/e-gly) ). La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immédiatement suivie des données de clé.<br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_ \_ objet blob de clé opaque BCRYPT \_**</dt> </dl> | Exporter une [*clé symétrique*](/windows/desktop/SecGloss/s-gly) dans un format spécifique à un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) unique. Les objets BLOB opaques ne sont pas transférables et doivent être importés à l’aide du CSP qui a généré l’objet BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_objet BLOB RSAPUBLIC de BCRYPT \_**</dt> </dl>     | Exportez une clé publique [*RSA*](/windows/desktop/SecGloss/r-gly) . La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immédiatement suivie des données de clé.<br/>                                                                                                                                                                                 |



 

</dd> <dt>

*pbKeyBlob* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon qui contient l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly).

</dd> <dt>

*cbKeyBlob* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbKeyBlob* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le descripteur *hSslProvider* n’est pas valide.<br/>                       |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phKey* a la **valeur null**.<br/>                            |



 

## <a name="remarks"></a>Remarques

Vous pouvez utiliser la fonction **SslImportKey** pour importer des clés de session dans le cadre du processus de transfert des clés de session d’un processus à un autre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

