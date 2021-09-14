---
description: Signe et heure marque le fichier spécifié, en autorisant plusieurs signatures imbriquées.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237486"
---
# <a name="signersignex2-function"></a>SignerSignEx2 fonction)

La fonction **SignerSignEx2** signe et met en cache l’heure du fichier spécifié, en autorisant plusieurs signatures imbriquées.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
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

Modifie le comportement de cette fonction.

Si le fichier à signer est un fichier exécutable portable (PE), il peut s’agir de zéro ou d’une combinaison d’une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Indicateur de hachages de page PE exclure**</dt> <dt>0x10</dt> </dl>                    | Excluez les hachages de page lors de la création de données SIP indirectes pour le fichier PE. Cet indicateur est prioritaire par rapport à l’indicateur d' **\_ indicateur de \_ \_ \_ hachage \_ de page PE Inc** .<br/> Si vous ne spécifiez pas l’indicateur de **\_ \_ \_ \_ hachages \_ de page de hachage de page PE de SPC exclure** ou si l’indicateur de **\_ \_ \_ \_ hachage \_ de page PE Inc** . est spécifié, la valeur définie avec la fonction [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) est utilisée pour ce paramètre. La valeur par défaut de ce paramètre est d’exclure les hachages de page lors de la création de données SIP indirectes pour les fichiers PE.<br/> Cette valeur est définie dans le fichier d’en-tête Mssip. h.<br/> **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ \_Indicateur de \_ \_ \_ table \_ addr d’importation PE Inc**</dt> <dt></dt> </dl> | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ \_Indicateur d' \_ \_ informations de \_ DÉbogage PE de Inc**</dt> . <dt></dt> </dl>                       | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ \_Indicateur de \_ ressources \_ PE Inc**</dt> . <dt></dt> </dl>                           | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Identificateurs de hachage de page PE de Inc**</dt> . <dt></dt> </dl>                   | Inclure les hachages de page lors de la création de données SIP indirectes pour le fichier PE.<br/> **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> Cette valeur est définie dans le fichier d’en-tête Mssip. h.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_ Ajouter**</dt> <dt>0x1000</dt> </dl>                                                                         | La signature sera imbriquée. Si vous définissez cet indicateur avant l’ajout d’une signature, la signature générée sera ajoutée en tant que signature externe. Si vous ne définissez pas cet indicateur, la signature générée remplace la signature externe, en supprimant toutes les signatures internes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

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

Pointeur vers une structure d' [**\_ \_ informations de fournisseur de signataires**](signer-provider-info.md) qui spécifie le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) et les informations de clé privée utilisés pour créer la signature numérique.

Si la valeur de ce paramètre est **null**, le paramètre *pSignerCert* doit spécifier un certificat associé à un CSP.

</dd> <dt>

*dwTimestampFlags* \[ dans, facultatif\]
</dt> <dd>

Indicateurs qui seront passés à [**SignerTimeStampEx3**](signertimestampex3.md) si le paramètre *pwszHttpTimeStamp* n’a pas la **valeur null**. Il peut s’agir de l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                          | Signification                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**AUTHENTICODE de l’horodateur du signataire \_ \_**</dt> </dl> | Valeur par défaut. Spécifie un horodateur Authenticode.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**Horodatage du \_ signataire \_ RFC3161**</dt> </dl>                | Spécifie un horodateur RFC 3161.<br/>                    |



 

Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* a la **valeur null**.

</dd> <dt>

*pszTimestampAlgorithmOid* \[ dans, facultatif\]
</dt> <dd>

Identificateur d’objet de l’algorithme à utiliser pour créer un horodateur RFC 3161. Ce paramètre est ignoré pour les horodatages Authenticode.

</dd> <dt>

*pwszHttpTimeStamp* \[ dans, facultatif\]
</dt> <dd>

URL du serveur d’horodatage.

</dd> <dt>

*psRequest* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un tableau de structures d' [**\_ attributs**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) de chiffre qui sont ajoutées à une demande de signature. Ce paramètre est ignoré si le paramètre *pwszHttpTimeStamp* ne contient pas de valeur valide ou a la valeur **null**.

</dd> <dt>

*pSipData* \[ dans, facultatif\]
</dt> <dd>

Valeur 32 bits qui est passée en tant que données supplémentaires aux fonctions SIP. Le format et le contenu de ce sont définis par le fournisseur SIP.

</dd> <dt>

*ppSignerContext* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l' [*objet BLOB*](../secgloss/b-gly.md)signé. Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez la structure du **\_ contexte du signataire** en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ dans, facultatif\]
</dt> <dd>

S’il est présent, pointeur vers une structure de [**\_ \_ \_ paragraphe de signe fort de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) qui contient les paramètres utilisés pour vérifier les signatures fortes. Si un certificat ou sa chaîne ne réussissent pas, le fichier n’est pas modifié de quelque manière que ce soit. Si une URL est transmise pour spécifier une autorité d’horodatage (TSA), cette stratégie est également appliquée à l’horodatage.

</dd> <dt>

*Respecté* 
</dt> <dd>

Réservé. Cette valeur doit être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction s’exécute correctement, la fonction retourne la valeur \_ OK.

Si la fonction échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Les codes d’erreur possibles retournés par cette fonction incluent, mais ne sont pas limités à, les éléments suivants. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).



| Code de retour                                                                                  | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si vous définissez le paramètre *dwTimestampFlags* sur **signer \_ timestamp \_ AUTHENTICODE**, vous ne pouvez pas définir le paramètre *dwFlags* sur **SIG \_ Append**.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
