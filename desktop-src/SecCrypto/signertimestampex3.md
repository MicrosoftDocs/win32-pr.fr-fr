---
description: Horodatage l’objet spécifié et prend en charge la définition des horodatages sur plusieurs signatures.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7eb5c19292b451b1a3d0265da4bb178eafcc6f00
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468556"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3 fonction)

L’heure de la fonction **SignerTimeStampEx3** marque l’objet spécifié et prend en charge la définition des horodatages sur plusieurs signatures.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateur qui spécifie le type d’horodatage à générer. Ce paramètre peut prendre les valeurs suivantes. Les valeurs s’excluent mutuellement.




| Valeur | Signification | 
|-------|---------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt></dl> | Spécifie un horodatage Authenticode.<br /><blockquote>[!Note]<br />Authenticode n’est plus le type d’horodatage préféré. La prise en charge des horodatages Authenticode peut être supprimée à l’avenir. Nous vous recommandons d’utiliser à la place la RFC 3161.</blockquote><br /> | 
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt></dl> | Spécifie un horodatage conforme à la norme RFC 3161.<br /> | 




 

</dd> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Spécifie le numéro de séquence de la signature à laquelle l’horodateur sera ajouté. Si cette valeur est égale à zéro (0), la signature externe sera horodatage.

</dd> <dt>

*pSubjectInfo* \[ dans\]
</dt> <dd>

Adresse d’une structure d' [**\_ \_ informations de sujet du signataire**](signer-subject-info.md) qui représente l’objet à horodater.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans\]
</dt> <dd>

Adresse d’une chaîne Unicode terminée par le caractère null qui contient l’URL d’un serveur d’horodatage.

</dd> <dt>

*pszAlgorithmOid* \[ dans\]
</dt> <dd>

Algorithme de hachage à utiliser pour exécuter des horodatages conformes à la norme RFC 3161. Ce paramètre est ignoré pour les horodatages Authenticode.

</dd> <dt>

*psRequest* \[ dans, facultatif\]
</dt> <dd>

facultatif. Adresse d’une structure [**d' \_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) de chiffre qui contient des attributs supplémentaires ajoutés à la demande d’horodatage.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*pSipData* \[ dans, facultatif\]
</dt> <dd>

facultatif. Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions du [*package d’interface de sujet*](../secgloss/s-gly.md) (SIP). Le format et le contenu de ce paramètre sont définis par le fournisseur SIP.

Ce paramètre est facultatif et peut avoir la **valeur null** s’il n’est pas inclus.

</dd> <dt>

*ppSignerContext* \[ à\]
</dt> <dd>

facultatif. Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l’objet BLOB signé. Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez-la en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ dans, facultatif\]
</dt> <dd>

S’il est présent, pointeur vers une structure de [**\_ \_ \_ paragraphe de signe fort de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) qui contient les paramètres utilisés pour vérifier les signatures fortes. L’horodatage doit passer cette stratégie de chiffrement.

</dd> <dt>

*Respecté* 
</dt> <dd>

Réservé. Cette valeur doit être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Les codes d’erreur possibles retournés par cette fonction incluent, mais ne sont pas limités à, les éléments suivants. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).




| Code de retour | Description | 
|-------------|-------------|
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Cette erreur peut être retournée pour les conditions suivantes :<br /><ul><li>Vous devez définir <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> ou <strong>SIGNER_TIMESTAMP_RFC3161</strong> pour le paramètre <em>dwFlags</em> .</li><li>Le paramètre <em>conserved</em> doit avoir la <strong>valeur null</strong>.</li><li>Si vous définissez l’indicateur <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> dans le paramètre <em>dwFlags</em> , vous devez définir le paramètre <em>dwIndex</em> sur zéro.</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
