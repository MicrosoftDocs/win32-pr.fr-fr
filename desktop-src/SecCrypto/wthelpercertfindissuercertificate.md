---
description: Recherche un certificat d’émetteur à partir des magasins de certificats spécifiés qui correspondent au certificat d’objet spécifié.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413434"
---
# <a name="wthelpercertfindissuercertificate-function"></a>WTHelperCertFindIssuerCertificate fonction)

\[La fonction **WTHelperCertFindIssuerCertificate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La fonction **WTHelperCertFindIssuerCertificate** recherche un certificat d’émetteur parmi les magasins de certificats spécifiés qui correspondent au certificat d’objet spécifié.

> [!Note]  
> Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Wintrust.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pChildContext* \[ dans\]
</dt> <dd>

Certificat d’objet pour lequel Rechercher un certificat d’émetteur correspondant.

</dd> <dt>

*chStores* \[ dans\]
</dt> <dd>

Nombre d’éléments dans le tableau *pahStores* .

</dd> <dt>

*pahStores* \[ dans\]
</dt> <dd>

Tableau de magasins de certificats dans lequel effectuer la recherche.

</dd> <dt>

*psftVerifyAsOf* \[ dans\]
</dt> <dd>

Heure de vérification.

</dd> <dt>

*dwEncoding* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui spécifie les types d’encodage du certificat à vérifier. Pour plus d’informations sur les types d’encodage possibles, consultez [types d’encodage de message et de certificat](certificate-and-message-encoding-types.md).

</dd> <dt>

*pdwConfidence* \[ out, facultatif\]
</dt> <dd>

Ce paramètre peut être une combinaison d’opérations de bits de zéro ou plusieurs des valeurs de confiance suivantes.



| Valeur                                                                                                                                                                                                                                                                 | Signification                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <dt>**Certificat \_ CONFIANCE \_ SIG**</dt> <dt> 0x10000000</dt> </dl>                     | La signature du certificat est valide.<br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <dt>**Certificat \_ \_Temps de confiance**</dt> <dt> 0x01000000</dt> </dl>                  | L’heure de l’émetteur du certificat est valide.<br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <dt> **Certificat \_ confidence \_ TIMENEST**</dt> <dt>0x00100000</dt> </dl>    | L’heure du certificat est valide.<br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <dt> **Certificat \_ confidence \_ AUTHIDEXT**</dt> <dt>0x00010000</dt> </dl> | L’extension de l’ID d’autorité est valide.<br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <dt> **Certificat \_ d' \_ hygiène de confiance**</dt> <dt>0x00001000</dt> </dl>       | Au minimum, la signature de l’extension Certificate and Authority ID est valide.<br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <dt> **Confiance du certificat \_ \_ le plus élevé**</dt> <dt>0x11111000</dt> </dl>       | Combinaison de toutes les autres valeurs de confiance.<br/>                                 |



 

</dd> <dt>

*dwError* \[ à\]
</dt> <dd>

Pointeur vers une variable **DWORD** qui contient la valeur d’erreur de ce certificat, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Certificat d’émetteur qui correspond au certificat de sujet spécifié par le paramètre *pChildContext* .

## <a name="remarks"></a>Notes

Pour trouver un certificat d’émetteur correspondant, les conditions suivantes doivent être remplies :

-   La signature du certificat objet spécifié par le paramètre *pChildContext* doit être valide.
-   Le membre **rgExtension** du membre **PCertInfo** du paramètre *pChildContext* doit contenir une structure d' [**informations d' \_ ID de clé d’autorité \_ \_ \_ de certification**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) . Les membres **CertIssuer** et **CertSerialMember** de cette structure correspondent davantage aux membres correspondants pour le certificat de l’émetteur.
-   La valeur du paramètre *psftVerifyAsOf* doit être comprise dans la période de validité du certificat du sujet.
-   La période de validité du certificat d’objet doit être comprise dans la période de validité du certificat de l’émetteur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
