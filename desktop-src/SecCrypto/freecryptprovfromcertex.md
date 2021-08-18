---
description: 'Libère le descripteur d’un fournisseur de services de chiffrement (CSP) ou d’une clé Cryptography API : Next Generation (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: b887fd7cd37e8963430378590552273b0856dc2cf73e9d0da15ab41a5a622447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006737"
---
# <a name="freecryptprovfromcertex-function"></a>FreeCryptProvFromCertEx fonction)

La fonction **FreeCryptProvFromCertEx** libère le descripteur d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) ou d’une clé Cryptography API : Next Generation (CNG).

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fAcquired* \[ dans\]
</dt> <dd>

Valeur qui spécifie si le handle du fournisseur a été acquis à partir du [*certificat*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ dans\]
</dt> <dd>

Handle vers un CSP CAPICOM ou un handle vers une clé CNG.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

Adresse d’une variable **DWORD** qui reçoit des informations supplémentaires sur la clé. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                | Signification                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**au niveau de \_ KEYexchange**</dt> </dl>                     | La paire de clés est une paire d’échange de clés.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**à la \_ signature**</dt> </dl>                           | La paire de clés est une paire de signatures.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**spécification de clé de certificat \_ NCRYPT \_ \_**</dt> </dl> | La clé est une clé CNG.<br/> **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null pour le nom du fournisseur.

</dd> <dt>

*dwProviderType* \[ dans\]
</dt> <dd>

Spécifie le type de fournisseur de services de chiffrement. Il peut s’agir de zéro ou de l’un des [types de fournisseur de chiffrement](cryptographic-provider-types.md). Si ce membre est égal à zéro, le conteneur de clé est l’un des fournisseurs de stockage de clés CNG.

</dd> <dt>

*pwszTmpContainer* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null pour le nom du conteneur de clé temporaire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
