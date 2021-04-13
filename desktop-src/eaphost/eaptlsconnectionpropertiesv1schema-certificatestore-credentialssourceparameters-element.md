---
title: Élément CertificateStore (CredentialsSourceParameters)
description: Indique que le protocole EAP-TLS doit lire le certificat du magasin My de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Élément CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508945"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>Élément CertificateStore (CredentialsSourceParameters)

L’élément **CertificateStore (CredentialsSourceParameters)** indique que le protocole EAP-TLS doit lire le certificat du magasin My de l’utilisateur ou de l’ordinateur en cours d’authentification.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

L’élément **CertificateStore** est défini par le type complexe [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .

## <a name="remarks"></a>Notes

Les éléments **CertificateStore** et [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ne peuvent pas être utilisés simultanément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





