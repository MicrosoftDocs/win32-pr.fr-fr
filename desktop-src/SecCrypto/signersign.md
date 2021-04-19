---
description: Signe le fichier spécifié.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522087"
---
# <a name="signersign-function"></a>SignerSign fonction)

La fonction **SignerSign** signe le fichier spécifié.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSubjectInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui spécifie l’objet à signer.

</dd> <dt>

*pSignerCert* \[ dans\]
</dt> <dd>

Pointeur vers une structure de [**\_ certificat de signataire**](signer-cert.md) qui spécifie le certificat à utiliser pour créer la signature numérique.

</dd> <dt>

*pSignatureInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de signature de signataire**](signer-signature-info.md) qui contient des informations sur la signature numérique.

</dd> <dt>

*pProviderInfo* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ informations de fournisseur de signataires**](signer-provider-info.md) qui spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de [*clé privée*](../secgloss/p-gly.md) utilisés pour créer la signature numérique.

Si la valeur de ce paramètre est **null**, la valeur du paramètre *pSignerCert* doit spécifier un certificat associé à un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans, facultatif\]
</dt> <dd>

URL d’un serveur d’horodatage.

</dd> <dt>

*psRequest* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un tableau de structures [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) de chiffre qui sont ajoutées à une demande de signature. Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* ne contient pas de valeur valide qui n’est pas **null**.

</dd> <dt>

*pSipData* \[ dans, facultatif\]
</dt> <dd>

Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP. Le format et le contenu de ce sont définis par le fournisseur SIP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
