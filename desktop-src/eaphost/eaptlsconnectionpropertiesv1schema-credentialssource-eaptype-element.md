---
title: Élément CredentialsSource (EapType)
description: En savoir plus sur l’élément CredentialsSource (EapType). Cet élément contient des informations sur l’emplacement du certificat EAP-TLS.
ms.assetid: 6ef48e5e-7c71-472f-ab01-0a43a97ecd96
keywords:
- Élément CredentialsSource EAPHost
topic_type:
- apiref
api_name:
- CredentialsSource
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d68eccf44b7e2c248e366d8e3d8f05f4e7dd4774
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106538997"
---
# <a name="credentialssource-eaptype-element"></a>Élément CredentialsSource (EapType)

L’élément **CredentialsSource (EapType)** contient des informations sur l’emplacement du certificat EAP-TLS.

``` syntax
<xs:element name="CredentialsSource"
    type="CredentialsSourceParameters"
 />
```

L’élément **CredentialsSource** est défini par l’élément [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Notes

L’élément **CredentialSource** est facultatif.

## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





