---
description: Horodatage l’objet spécifié et retourne éventuellement un pointeur vers une structure de contexte de signataire \_ qui contient un pointeur vers un objet BLOB. Cette fonction peut être utilisée pour effectuer une infrastructure à clé publique X. 509, RFC 3161&\# 8211 ; conforme, horodatage.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522164"
---
# <a name="signertimestampex2-function"></a>SignerTimeStampEx2 fonction)

L’heure de la fonction **SignerTimeStampEx2** marque l’objet spécifié et retourne éventuellement un pointeur vers une structure de [**\_ contexte de signataire**](signer-context.md) qui contient un pointeur vers un [*objet BLOB*](../secgloss/b-gly.md). Cette fonction peut être utilisée pour effectuer l’infrastructure de clé publique X. 509, conforme à la norme RFC 3161, horodatage.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Valeur qui spécifie le type d’horodatage à générer. Ce paramètre peut prendre les valeurs suivantes. Les valeurs s’excluent mutuellement.



| Valeur                                                                                                                                                                                                          | Signification                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**AUTHENTICODE de l’horodateur du signataire \_ \_**</dt> </dl> | Spécifie un horodatage Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**Horodatage du \_ signataire \_ RFC3161**</dt> </dl>                | Spécifie un horodatage conforme à la norme RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ dans\]
</dt> <dd>

Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans\]
</dt> <dd>

Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.

</dd> <dt>

*dwAlgId* \[ dans\]
</dt> <dd>

Spécifie un algorithme de hachage à utiliser pour exécuter des horodatages conformes à la norme RFC 3161. Ce paramètre est ignoré pour les horodatages Authenticode.

</dd> <dt>

*psRequest* \[ dans\]
</dt> <dd>

Optionnel. Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*pSipData* \[ dans\]
</dt> <dd>

Optionnel. Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP). Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*ppSignerContext* \[ à\]
</dt> <dd>

Optionnel. Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé. Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
