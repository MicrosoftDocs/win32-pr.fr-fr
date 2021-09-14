---
description: Horodatage l’objet spécifié et retourne éventuellement un pointeur vers une structure de contexte de signataire \_ qui contient un pointeur vers un objet BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237474"
---
# <a name="signertimestampex-function"></a>SignerTimeStampEx fonction)

L’heure de la fonction **SignerTimeStampEx** marque l’objet spécifié et retourne éventuellement un pointeur vers une structure de [**\_ contexte de signataire**](signer-context.md) qui contient un pointeur vers un [*objet BLOB*](../secgloss/b-gly.md). Cette fonction prend en charge l’horodatage Authenticode. Pour effectuer l’horodatage de l’infrastructure à clé publique (RFC 3161) X. 509, utilisez la fonction [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé. Ce paramètre doit avoir la valeur zéro.

</dd> <dt>

*pSubjectInfo* \[ dans\]
</dt> <dd>

Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans\]
</dt> <dd>

Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.

</dd> <dt>

*psRequest* \[ dans\]
</dt> <dd>

Optionnel. Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*pSipData* \[ dans\]
</dt> <dd>

facultatif. Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP). Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*ppSignerContext* \[ à\]
</dt> <dd>

Optionnel. Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé. Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> </dl>

 

 
