---
description: Définit les codes d’erreur retournés par CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Énumération CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: abdd2556ace3e3c3c82ccdeedc907d77f9ce1702
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121125"
---
# <a name="capicom_error_code-enumeration"></a>\_Énumération de code d’erreur CAPICOM \_

Le type d’énumération du **\_ \_ code d’erreur CAPICOM** définit les codes d’erreur retournés par CAPICOM.

> [!Note]  
> Visual Basic Les erreurs d’édition de script retournent une valeur **Err. Number** supérieure à zéro. Pour ces erreurs, les valeurs de **Err. Description** fournissent des informations sur la cause de l’erreur. en plus des erreurs d’édition de script Visual Basic, les erreurs capicom retournent les codes définis par le **\_ \_ CODE d’erreur capicom**.

 

## <a name="members"></a>Membres




| Membre | Description | Valeur | 
|--------|-------------|-------|
| <strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong> | Un type d’encodage non valide a été utilisé.<br /> La liste suivante répertorie les types d’encodage valides :<ul><li>CAPICOM_ENCODE_ANY</li><li>CAPICOM_ENCODE_BASE64</li><li>CAPICOM_ENCODE_BINARY</li></ul><br /> | 0x80880100 | 
| <strong>CAPICOM_E_EKU_INVALID_OID</strong> | La propriété <a href="eku-oid.md"><strong>OID</strong></a> de l’objet <a href="eku.md"><strong>EKU</strong></a> ne peut pas être définie, car la propriété <a href="eku-name.md"><strong>Name</strong></a> n’est pas définie sur CAPICOM_EKU_OTHER.<br /> Définissez la propriété <a href="eku-name.md"><strong>nom</strong></a> sur CAPICOM_EKU_OTHER avant de définir la propriété <a href="eku-oid.md"><strong>OID</strong></a> .<br /> | 0x80880200 | 
| <strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong> | La propriété <a href="eku-oid.md"><strong>OID</strong></a> de l’objet <a href="eku.md"><strong>EKU</strong></a> n’a pas été initialisée. <br /> Affectez à la propriété <a href="eku-name.md"><strong>Name</strong></a> une valeur autre que CAPICOM_EKU_OTHER, ou affectez à la propriété <strong>name</strong> la valeur CAPICOM_EKU_OTHER et à la propriété <a href="eku-oid.md"><strong>OID</strong></a> la valeur.<br /> | 0x80880201 | 
| <strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong> | L’objet de <a href="certificate.md"><strong>certificat</strong></a> n’a pas été initialisé.<br /> En règle générale, ce code d’erreur est retourné lorsqu’un objet de <a href="certificate.md"><strong>certificat</strong></a> est instancié, mais n’est pas associé à un certificat numérique. Pour associer l’objet à un certificat numérique, affectez-le à un objet de <strong>certificat</strong> existant ou appelez la méthode <a href="certificate-import.md"><strong>Import</strong></a> .<br /> | 0x80880210 | 
| <strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong> | L’objet <a href="certificate.md"><strong>certificat</strong></a> n’a pas de clé privée associée.<br /> Ce code d’erreur est retourné lorsqu’une tentative est faite pour signer des données à l’aide de la clé privée du signataire, mais l’objet de <a href="certificate.md"><strong>certificat</strong></a> associé à l’objet <a href="signer.md"><strong>signataire</strong></a> ne peut pas être utilisé pour l’opération de signature.<br /> | 0x80880211 | 
| <strong>CAPICOM_E_CHAIN_NOT_BUILT</strong> | L’objet de <a href="chain.md"><strong>chaîne</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet de <a href="chain.md"><strong>chaîne</strong></a> , appelez la méthode de <a href="chain-build.md"><strong>génération</strong></a> .<br /> | 0x80880220 | 
| <strong>CAPICOM_E_STORE_NOT_OPENED</strong> | L’objet <a href="store.md"><strong>Store</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet <a href="store.md"><strong>Store</strong></a> , appelez la méthode <a href="store-open.md"><strong>Open</strong></a> .<br /> | 0x80880230 | 
| <strong>CAPICOM_E_STORE_EMPTY</strong> | L’objet <a href="store.md"><strong>Store</strong></a> ne contient aucun objet de <a href="certificate.md"><strong>certificat</strong></a> .<br /> | 0x80880231 | 
| <strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong> | Le paramètre <em>OpenMode</em> de la méthode <a href="store-open.md"><strong>Store. Open</strong></a> ne contient pas de valeur valide de CAPICOM_STORE_OPEN_MODE.<br /> La liste suivante indique les valeurs valides de CAPICOM_STORE_OPEN_MODE :<ul><li>CAPICOM_STORE_OPEN_READ_ONLY</li><li>CAPICOM_STORE_OPEN_READ_WRITE</li><li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li><li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li><li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li></ul><br /> | 0x80880232 | 
| <strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong> | La valeur <em>SaveAs</em> transmise à la méthode d' <a href="store-export.md"><strong>exportation</strong></a> de l’objet <a href="store.md"><strong>Store</strong></a> n’est pas valide. <br /> La liste suivante affiche les valeurs <em>SaveAs</em> valides :<ul><li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li><li>CAPICOM_STORE_SAVE_AS_PKCS7</li></ul><br /> | 0x80880233 | 
| <strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong> | La propriété de <a href="attribute-name.md"><strong>nom</strong></a> de l’objet d' <a href="attribute.md"><strong>attribut</strong></a> n’a pas été initialisée. <br /> Définissez la propriété <a href="attribute-name.md"><strong>Name</strong></a> .<br /> | 0x80880240 | 
| <strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong> | La propriété <a href="attribute-value.md"><strong>value</strong></a> de l’objet <a href="attribute.md"><strong>attribut</strong></a> n’a pas été initialisée. <br /> Définissez la propriété <a href="attribute-value.md"><strong>value</strong></a> .<br /> | 0x80880241 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong> | La propriété de <a href="attribute-name.md"><strong>nom</strong></a> de l’objet d' <a href="attribute.md"><strong>attribut</strong></a> n’est pas valide. <br /> La liste suivante répertorie les noms d’attributs valides :<ul><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li></ul><br /> | 0x80880242 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong> | La propriété <a href="attribute-value.md"><strong>value</strong></a> de l’objet <a href="attribute.md"><strong>attribut</strong></a> n’est pas valide, car le type de données ne correspond pas au type de données indiqué par la propriété <strong>Name</strong> . <br /> Par exemple, si la propriété <a href="attribute-value.md"><strong>Name</strong></a> est définie sur CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, le type de données doit être <strong>Date</strong>.<br /> | 0x80880243 | 
| <strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong> | L’objet <a href="signer.md"><strong>signataire</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet <a href="signer.md"><strong>signataire</strong></a> , définissez la propriété <a href="signer-certificate.md"><strong>certificat</strong></a> .<br /> | 0x80880250 | 
| <strong>CAPICOM_E_SIGNER_NOT_FOUND</strong> | Le signataire est introuvable dans l’objet <a href="signeddata.md"><strong>SignedData</strong></a> . <br /> En règle générale, cela ne se produit pas avec un objet <a href="signeddata.md"><strong>SignedData</strong></a> qui a été créé par CAPICOM ; Toutefois, si l’objet <strong>SignedData</strong> a été créé par un produit tiers, le certificat du signataire peut ne pas être inclus dans la structure de #7 Pkcs.<br /> | 0x80880251 | 
| <strong>CAPICOM_E_SIGNER_NO_CHAIN</strong> | Un objet <a href="chain.md"><strong>chaîne</strong></a> est introuvable dans l’objet <a href="signer.md"><strong>signataire</strong></a> .<br /> | 0x80880252//v 2.0 | 
| <strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong> | Une tentative d’utilisation du signataire est effectuée de manière non valide.<br /> | 0x80880253.//v2.0 | 
| <strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong> | L’objet <a href="signeddata.md"><strong>SignedData</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet <a href="signeddata.md"><strong>SignedData</strong></a> , définissez la propriété <a href="signeddata-content.md"><strong>content</strong></a> ou appelez la méthode <a href="signeddata-verify.md"><strong>verify</strong></a> .<br /> | 0x80880260 | 
| <strong>CAPICOM_E_SIGN_INVALID_TYPE</strong> | L’objet <a href="signeddata.md"><strong>SignedData</strong></a> contient un type qui n’est pas valide. <br /> En règle générale, cela se produit lorsqu’une tentative est effectuée pour vérifier un message enveloppé avec un objet <a href="signeddata.md"><strong>SignedData</strong></a> ou vice versa.<br /> | 0x80880261 | 
| <strong>CAPICOM_E_SIGN_NOT_SIGNED</strong> | L’objet <a href="signeddata.md"><strong>SignedData</strong></a> n’a pas été signé. <br /> Pour signer l’objet <a href="signeddata.md"><strong>SignedData</strong></a> , appelez la méthode <a href="signeddata-sign.md"><strong>Sign</strong></a> .<br /> | 0x80880262 | 
| <strong>CAPICOM_E_INVALID_ALGORITHM</strong> | La valeur de l’algorithme pour la propriété <a href="algorithm-name.md"><strong>Name</strong></a> de l’objet <a href="algorithm.md"><strong>algorithme</strong></a> n’est pas valide. <br /> La liste suivante indique les valeurs d’algorithme valides pour la propriété <a href="algorithm-name.md"><strong>Name</strong></a> :<ul><li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li><li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li><li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li><li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li></ul><br /> | 0x80880270 | 
| <strong>CAPICOM_E_INVALID_KEY_LENGTH</strong> | La valeur de la longueur de clé de la propriété <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> de l’objet <a href="algorithm.md"><strong>algorithme</strong></a> n’est pas valide. <br /> La liste suivante indique les valeurs de longueur de clé valides pour la propriété <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> :<ul><li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li></ul><br /> | 0x80880271 | 
| <strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong> | L’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , définissez la propriété <a href="envelopeddata-content.md"><strong>content</strong></a> ou appelez la méthode <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .<br /> | 0x80880280 | 
| <strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong> | L’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contient un type qui n’est pas valide. <br /> En règle générale, cela se produit lorsqu’une tentative est effectuée pour vérifier un message signé avec un objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> ou vice versa.<br /> | 0x80880281 | 
| <strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong> | Aucun destinataire n’est spécifié dans l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> lorsque la méthode <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> d’un objet <strong>EnvelopedData</strong> est appelée. <br /> Pour ajouter un destinataire, appelez la méthode <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .<br /> | 0x80880282 | 
| <strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong> | Le destinataire est introuvable dans l’objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> . <br /> En règle générale, cela ne se produit pas avec un objet <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> qui a été créé par CAPICOM ; Toutefois, si l’objet <strong>EnvelopedData</strong> a été créé par un produit tiers, le certificat du destinataire peut ne pas être inclus dans la structure de #7 Pkcs.<br /> | 0x80880283 | 
| <strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong> | L’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’a pas été initialisé. <br /> Pour initialiser l’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , définissez la propriété de <a href="encrypteddata-content.md"><strong>contenu</strong></a> ou appelez la méthode <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .<br /> | 0x80880290 | 
| <strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong> | L’objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’est pas un type valide. <br /> En règle générale, cela signifie que les données sont endommagées.<br /> | 0x80880291 | 
| <strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong> | Le secret d’un objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> n’a pas été initialisé. <br /> Pour initialiser le secret d’un objet <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , appelez la méthode <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> .<br /> | 0x80880292 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong> | L’objet <a href="privatekey.md"><strong>PrivateKey</strong></a> n’a pas été initialisé.<br /> | 0x80880300//v 2.0 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong> | Impossible d’exporter l’objet <a href="privatekey.md"><strong>PrivateKey</strong></a> .<br /> | 0x80880301//v 2.0 | 
| <strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong> | L’objet <a href="encodeddata.md"><strong>EncodedData</strong></a> n’a pas été initialisé.<br /> | 0x80880320//v 2.0 | 
| <strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong> | L’objet d' <a href="extension.md"><strong>extension</strong></a> n’a pas été initialisé.<br /> | 0x80880330//v 2.0 | 
| <strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong> | La propriété <a href="extendedproperty-propid.md"><strong>propid</strong></a> de l’objet <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> n’a pas été initialisée.<br /> | 0x80880340//v 2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_TYPE</strong> | Le paramètre <em>FindType</em> de la méthode <a href="certificates-find.md"><strong>Certificates. Find</strong></a> n’est pas une valeur de l’énumération <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .<br /> | 0x80880350//v 2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong> | La stratégie prédéfinie spécifiée pour l’opération de recherche n’est pas valide.<br /> | 0x80880351//v 2.0 | 
| <strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong> | L’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisé.<br /> | 0x80880360//v 2.0 | 
| <strong>CAPICOM_E_CODE_NOT_SIGNED</strong> | L’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été signé.<br /> Pour signer l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> , appelez la méthode <a href="signedcode-sign.md"><strong>Sign</strong></a> .<br /> | 0x80880361//v 2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong> | La propriété <a href="signedcode-description.md"><strong>Description</strong></a> de l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisée.<br /> | 0x80880362//v 2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong> | La propriété <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> de l’objet <a href="signedcode.md"><strong>SignedCode</strong></a> n’a pas été initialisée.<br /> | 0x80880363//v 2.0 | 
| <strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong> | Le paramètre d' <em>URL</em> de la méthode <a href="signedcode-timestamp.md"><strong>SignedCode. Timestamp</strong></a> n’est pas valide.<br /> | 0x80880364//v 2.0 | 
| <strong>CAPICOM_E_HASH_NO_DATA</strong> | L’objet <a href="hasheddata.md"><strong>HashedData</strong></a> ne contient aucune donnée.<br /> | 0x80880370//v 2.0 | 
| <strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong> | Le type de conversion n’est pas valide.<br /> | 0x80880380//v 2.0 | 
| <strong>CAPICOM_E_NOT_SUPPORTED</strong> | L’opération demandée n’est pas prise en charge dans la plateforme actuelle. <br /> | 0x80880900 | 
| <strong>CAPICOM_E_UI_DISABLED</strong> | Lors de la signature, la propriété <a href="signer-certificate.md"><strong>Certificate</strong></a> de l’objet <a href="signer.md"><strong>signataire</strong></a> n’a pas été définie, mais l’invite du certificat utilisateur a été désactivée. <br /> activez l’invite en définissant la propriété <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> de l’objet <a href="settings.md"><strong>Paramètres</strong></a> ou définissez la propriété <a href="signer-certificate.md"><strong>certificat</strong></a> de l’objet <a href="signer.md"><strong>signataire</strong></a> .<br /> | 0x80880901 | 
| <strong>CAPICOM_E_CANCELLED</strong> | L’opération a été annulée par l’utilisateur. <br /> Cela se produit lorsque l’utilisateur est invité à autoriser l’exécution d’une certaine opération, par exemple l’accès à la clé privée, et que l’utilisateur annule l’opération.<br /> | 0x80880902 | 
| <strong>CAPICOM_E_NOT_ALLOWED</strong> | L’opération tentée n’est pas autorisée.<br /> Par exemple, la modification de la propriété <a href="extendedproperty-propid.md"><strong>propid</strong></a> d’un objet <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> n’est pas autorisée si l’objet est attaché à un certificat.<br /> | 0x80880903//v 2.0 | 
| <strong>CAPICOM_E_OUT_OF_RESOURCE</strong> | CAPICOM n’a plus de ressources.<br /> | 0x80880904//v 2.0 | 
| <strong>CAPICOM_E_INTERNAL</strong> | Une erreur interne s'est produite. <br /> Contactez le support technique Microsoft pour obtenir de l’aide.<br /> | 0x80880911 | 
| <strong>CAPICOM_E_UNKNOWN</strong> | Une erreur inconnue s’est produite. <br /> Collectez autant d’informations que possible et contactez votre fournisseur.<br /> | 0x80880999 | 




## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




