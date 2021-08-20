---
title: Élément SimpleCertSelection (CertSelection)
description: En savoir plus sur l’élément SimpleCertSelection (CertSelection). Cet élément détermine la façon dont l’utilisateur sélectionne un certificat.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Élément SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f90f13f30ab467b4383e74bc85456ff0691bbb92dfa38e0d1f2c8f1f2f92f7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720216"
---
# <a name="simplecertselection-certselection-element"></a>Élément SimpleCertSelection (CertSelection)

L’élément **SimpleCertSelection (CertSelection)** détermine la façon dont l’utilisateur sélectionne un certificat.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

L’élément **SimpleCertSelection** est défini par le type complexe [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .

## <a name="remarks"></a>Remarques

**SimpleCertSelection** a la valeur true par défaut. Si **SimpleCertSelection** a la valeur true, EAP-TLS effectue une recherche de certificat simple sans liste déroulante pour la sélection des certificats. Si **SimpleCertSelection** a la valeur false, EAP-TLS illustre à l’utilisateur le certificat approprié à sélectionner.

## <a name="requirements"></a>Conditions requises



| Role | Système d’exploitation minimal pris en charge |
|------|----------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**CertificateStore (CredentialsSourceParameters)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





