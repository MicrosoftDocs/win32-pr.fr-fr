---
description: Supprime une propriété étendue de la collection.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: ExtendedProperties. Remove, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 684d5abc0a0114e0d2bedb0dc544d50e13337631bb41fb457480dfbe8c5364e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007217"
---
# <a name="extendedpropertiesremove-method"></a>ExtendedProperties. Remove, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **Remove** supprime une propriété étendue de la collection.

## <a name="syntax"></a>Syntaxe


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*propID* \[ dans\]
</dt> <dd>

Valeur de l’énumération [**\_ propid propid**](capicom-propid.md) qui définit les identificateurs de propriété CAPICOM de la propriété étendue à supprimer. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**\_propid propid \_ inconnu**</dt> </dl>                                                                       | Le type de la propriété n’est pas connu.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**CAPICOM-handle de clé de l’ID de la \_ \_ \_ preuve \_**</dt> </dl>                                             | Handle d’un conteneur de clé dans un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**CAPICOM- \_ \_ \_ informations sur la clé \_ de l’ID de la clé**</dt> </dl>                                                   | Informations sur un conteneur de clé dans un fournisseur de services de chiffrement.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**\_ \_ Hachage SHA1 du CAPICOM \_**</dt> </dl>                                                                | Objet de hachage SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**\_Prop. ID de \_ hachage de CAPICOM \_**</dt> </dl>                                                                | Propriétés d’un objet de hachage.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**\_ \_ Hachage MD5 du CAPICOM \_**</dt> </dl>                                                                   | Objet de hachage MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**contexte de clé de l’ID de la \_ \_ clé CAPICOM \_**</dt> </dl>                                                          | [*Contexte*](../secgloss/c-gly.md)de clé.<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**spécification de clé de CAPICOM \_ propid \_ \_**</dt> </dl>                                                                   | Spécifications pour une clé.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**\_Ie30 propid propid \_ \_ réservé**</dt> </dl>                                                    | Informations indiquant si l’objet est réservé dans Internet Explorer 3,0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**CAPICOM PUBKEY de \_ \_ \_ hachage \_ réservé**</dt> </dl>                              | Informations indiquant si le hachage de la clé publique est réservé.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**\_utilisation de ENHKEY propid \_ propid \_**</dt> </dl>                                                       | [*Utilisation améliorée*](../secgloss/e-gly.md) de la clé (EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**\_ \_ utilisation CTL de CAPICOM propid \_**</dt> </dl>                                                                | Utilisation d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**\_ \_ \_ emplacement de mise à jour suivant \_ de CAPICOM propid**</dt> </dl>                              | Emplacement de la prochaine mise à jour de la [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**\_ \_ nom convivial de l’propid \_ CAPICOM**</dt> </dl>                                                    | Nom explicite.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**\_fichier baproper propid \_ pvk \_**</dt> </dl>                                                                   | Fichier qui contient une clé privée.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**Description de l' \_ propid \_ CAPICOM**</dt> </dl>                                                           | Description explicite.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**\_ \_ État d’accès à CAPICOM \_ propid**</dt> </dl>                                                       | État de l’accès.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**hachage de la \_ signature propid de CAPICOM \_ \_**</dt> </dl>                                                 | Hachage de la signature.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**\_ \_ données de carte à puce \_ de CAPICOM propid \_**</dt> </dl>                                             | Données de carte à puce.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**CAPICOM \_ ID prop \_ EFS**</dt> </dl>                                                                                   | Un système de fichiers EFS (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**informations de l' \_ ID de l’propid \_ \_**</dt> </dl>                                                    | Données créées à l’aide des protocoles et algorithmes de chiffrement détenus par le [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**\_propid propid \_ Archivé**</dt> </dl>                                                                    | Informations indiquant si l’objet est archivé.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**identificateur de clé de l’ID de la \_ \_ clé CAPICOM \_**</dt> </dl>                                                 | Identificateur de clé.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**\_ \_ inscription automatique de CAPICOM propid \_**</dt> </dl>                                                          | Informations d’inscription automatique pour un certificat.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**\_ \_ PUBKEY \_ ALG- \_ parase propid**</dt> </dl>                                             | Paramètres d’un algorithme de clé publique.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**les points de \_ \_ distribution du \_ CERT \_ de \_ CAPICOM**</dt> </dl>                       | Informations utilisées pour mettre à jour les certificats croisés dynamiques.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**\_Hachage MD5 de la \_ \_ \_ clé publique \_ \_ de l’émetteur du propid-CAPICOM**</dt> </dl>          | Hachage MD5 de la clé publique de l’émetteur.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**\_Hachage MD5 de la \_ \_ clé publique du sujet \_ \_ de CAPICOM \_**</dt> </dl>       | Hachage MD5 de la clé publique du sujet.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**inscription à l' \_ ID d' \_ inscription CAPICOM**</dt> </dl>                                                              | Informations sur l’inscription du certificat.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**horodatage de la date d’affectation CAPICOM \_ \_ \_**</dt> </dl>                                                             | Marqueur de date.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ Hachage MD5 du numéro de série \_ de l’émetteur \_ CAPICOM**</dt> </dl> | Hachage MD5 du numéro de série de l’émetteur.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**\_ \_ \_ Hachage MD5 du nom d’objet \_ de l’ID de l’objet CAPICOM \_**</dt> </dl>                          | Hachage MD5 du nom du sujet.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_ \_ informations d’erreur étendues de l’propid de \_ CAPICOM \_**</dt> </dl>                                 | Informations étendues sur une erreur.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**Renouvellement de l’propid d’un CAPICOM \_ \_**</dt> </dl>                                                                       | Informations sur le renouvellement d’une [*autorité de certification*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**hachage de la \_ \_ clé archivée de l’ID de la \_ clé \_ CAPICOM**</dt> </dl>                                       | Hachage archivé d’une clé.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**Réservation d’une \_ propid d' \_ abord pour \_ CAPICOM**</dt> </dl>                                                 | Informations sur la première réservation.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**Réservation de l' \_ ID de la \_ dernière \_ réservation CAPICOM**</dt> </dl>                                                    | Informations sur la réservation la plus récente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**CAPICOM d’un \_ \_ premier \_ utilisateur**</dt> </dl>                                                             | Informations sur le premier utilisateur.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**CAPICOM \_ propr propid \_ dernier \_ utilisateur**</dt> </dl>                                                                | Informations sur l’utilisateur le plus récent.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
