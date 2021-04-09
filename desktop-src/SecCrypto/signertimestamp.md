---
description: Horodatage l’objet spécifié. Cette fonction prend en charge l’horodatage Authenticode. Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952701"
---
# <a name="signertimestamp-function"></a>SignerTimeStamp fonction)

L’heure de la fonction **SignerTimeStamp** marque l’objet spécifié. Cette fonction prend en charge l’horodatage Authenticode. Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSubjectInfo* \[ dans\]
</dt> <dd>

Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans\]
</dt> <dd>

Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.

</dd> <dt>

*psRequest* \[ dans, facultatif\]
</dt> <dd>

Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*pSipData* \[ dans, facultatif\]
</dt> <dd>

Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP. Le format et le contenu de ce sont définis par le fournisseur SIP.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

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



 

 
