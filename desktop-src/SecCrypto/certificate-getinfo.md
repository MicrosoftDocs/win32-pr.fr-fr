---
description: Récupère les informations du certificat.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2 :: GetInfo, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528432"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2 :: GetInfo, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **GetInfo** récupère les informations du [*certificat*](../secgloss/c-gly.md).

## <a name="syntax"></a>Syntaxe


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Infotype* \[ dans\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ \_ type informations du certificat CAPICOM**](capicom-cert-info-type.md) qui spécifie le type de données extraites du certificat. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                     | Signification                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**\_ \_ \_ \_ \_ nom simple de l’objet du certificat CAPICOM**</dt> </dl> | Retourne le nom complet de l’objet du certificat.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**\_ \_ \_ \_ \_ nom simple de l’émetteur d’informations de certificat CAPICOM**</dt> </dl>    | Retourne le nom complet de l’émetteur du certificat.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**nom du message de l’objet de l' \_ information du certificat CAPICOM \_ \_ \_ \_**</dt> </dl>    | Retourne l’adresse de messagerie de l’objet du certificat.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**nom de messagerie de l' \_ émetteur du certificat CAPICOM \_ info \_ \_ \_**</dt> </dl>       | Retourne l’adresse de messagerie de l’émetteur du certificat.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**UPN de l' \_ \_ objet d’informations de certificat CAPICOM \_ \_**</dt> </dl>                          | Retourne l’UPN de l’objet du certificat. Introduit dans CAPICOM 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**UPN de l' \_ \_ émetteur des informations de certificat CAPICOM \_ \_**</dt> </dl>                             | Retourne l’UPN de l’émetteur du certificat. Introduit dans CAPICOM 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**\_ \_ \_ \_ \_ nom DNS de l’objet du certificat CAPICOM**</dt> </dl>          | Retourne le nom DNS de l’objet du certificat. Introduit dans CAPICOM 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**\_ \_ \_ \_ nom DNS de l’émetteur CAPICOM informations CERT \_**</dt> </dl>             | Retourne le nom DNS de l’émetteur du certificat. Introduit dans CAPICOM 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Chaîne qui contient les informations demandées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Certificat**](certificate.md)
</dt> </dl>

 

 
