---
description: Retourne une clé de session de protocole SSL (Secure Sockets Layer) (SSL) ou une clé éphémère publique dans un objet BLOB sérialisé.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: SslExportKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951676"
---
# <a name="sslexportkey-function"></a>SslExportKey fonction)

La fonction **SslExportKey** retourne une [*clé de session*](/windows/desktop/SecGloss/s-gly) de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL) ou une clé éphémère publique dans un [*objet BLOB*](/windows/desktop/SecGloss/b-gly)sérialisé.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*HKEY* \[ dans\]
</dt> <dd>

Handle de la clé à exporter.

Si vous ne spécifiez pas de clé, affectez la valeur **null** à ce paramètre.

> [!Note]  
> Un handle *HKEY* est obtenu en appelant la fonction [**SslOpenPrivateKey**](sslopenprivatekey.md) . Les handles obtenus à partir de la fonction [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) ne sont pas pris en charge.

 

</dd> <dt>

*pszBlobType* \[ dans\]
</dt> <dd>

Chaîne Unicode terminée par le caractère null qui contient un identificateur spécifiant le type d’objet BLOB à exporter. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                      | Signification                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <dt>**\_ \_ objet BLOB public de BCRYPT DH \_**</dt> </dl>    | Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman. La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ \_ objet blob de clé**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) de la clé de données BCRYPT immédiatement suivie des données de clé.<br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <dt>**\_objet BLOB ECCPUBLIC de BCRYPT \_**</dt> </dl>     | Exportez une clé publique ECC ( [*Elliptic Curve Cryptography*](/windows/desktop/SecGloss/e-gly) ). La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immédiatement suivie des données de clé.<br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <dt>**\_ \_ objet blob de clé opaque BCRYPT \_**</dt> </dl> | Exporter une clé symétrique dans un format spécifique à un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) unique. Les objets BLOB opaques ne sont pas transférables et doivent être importés à l’aide du même *fournisseur de services de chiffrement* (CSP) qui a généré l’objet BLOB.<br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <dt>**\_objet BLOB RSAPUBLIC de BCRYPT \_**</dt> </dl>     | Exportez une clé publique RSA. La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immédiatement suivie des données de clé.<br/>                                                                                                                                                                                                |



 

</dd> <dt>

*pbOutput* \[ out, facultatif\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly). Le paramètre *cbOutput* contient la taille de cette mémoire tampon. Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Adresse d’une variable **DWORD** qui reçoit le nombre d’octets copiés dans la mémoire tampon *pbOutput* . Si le paramètre *pbOutput* a la valeur **null** lorsque la fonction est appelée, la taille requise pour la mémoire tampon *pbOutput* , en octets, est retournée dans la **valeur DWORD** désignée par ce paramètre.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé pour un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

La fonction **SslExportKey** facilite le transport des clés de session d’un processus à un autre, ainsi que l’exportation de la partie publique d’une clé éphémère.

Lorsque vous exportez des clés de session, le type d’objet BLOB est opaque, ce qui signifie que le format de l’objet BLOB n’a pas d’importance tant que les fonctions **SslExportKey** et [**SslImportKey**](sslimportkey.md) peuvent l’interpréter.

Lors de l’exportation de la partie publique d’une clé éphémère, le type d’objet BLOB doit être le type approprié, par exemple, l’objet BLOB **\_ \_ public \_** ou l' **\_ \_ objet BLOB ECCPUBLIC ncrypt**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

