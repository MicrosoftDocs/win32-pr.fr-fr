---
description: Signe le fichier spécifié et retourne un pointeur vers les données signées.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755564"
---
# <a name="signersignex-function"></a>SignerSignEx fonction)

La fonction **SignerSignEx** signe le fichier spécifié et retourne un pointeur vers les données signées.

> [!Note]  
> Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé. Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mssign32.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Modifie le comportement de cette fonction.

Si le fichier à signer est un fichier exécutable portable (PE), il peut s’agir de zéro ou d’une combinaison d’une ou plusieurs des valeurs suivantes. Ces identificateurs sont définis dans Mssip. h.



| Valeur                                                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Indicateur de hachages de page PE exclure**</dt> <dt>0x10</dt> </dl>                    | Excluez les hachages de page lors de la création de données SIP indirectes pour le fichier PE. Cet indicateur est prioritaire par rapport à l’indicateur d' **\_ indicateur de \_ \_ \_ hachage \_ de page PE Inc** .<br/> Si vous ne spécifiez pas l’indicateur de **\_ \_ \_ \_ hachages \_ de page de hachage de page PE de SPC exclure** ou si l’indicateur de **\_ \_ \_ \_ hachage \_ de page PE Inc** . est spécifié, la valeur définie avec la fonction [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) est utilisée pour ce paramètre. La valeur par défaut de ce paramètre est d’exclure les hachages de page lors de la création de données SIP indirectes pour les fichiers PE.<br/> **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ \_Indicateur de \_ \_ \_ table \_ addr d’importation PE Inc**</dt> <dt></dt> </dl> | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ \_Indicateur d' \_ \_ informations de \_ DÉbogage PE de Inc**</dt> . <dt></dt> </dl>                       | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ \_Indicateur de \_ ressources \_ PE Inc**</dt> . <dt></dt> </dl>                           | Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_ \_ \_ \_ Identificateurs de hachage de page PE de Inc**</dt> . <dt></dt> </dl>                   | Inclure les hachages de page lors de la création de données SIP indirectes pour le fichier PE.<br/> **Windows Server 2003 et Windows XP :** Cette valeur n’est pas prise en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

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

</dd> <dt>

*ppSignerContext* \[ à\]
</dt> <dd>

Adresse d’un pointeur vers la structure de [**\_ contexte du signataire**](signer-context.md) qui contient l' [*objet BLOB*](../secgloss/b-gly.md)signé. Lorsque vous avez terminé d’utiliser la structure du **\_ contexte du signataire** , libérez la structure du **\_ contexte du signataire** en appelant la fonction [**SignerFreeSignerContext**](signerfreesignercontext.md) .

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

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
