---
title: Élément UserCert (EapType)
description: Fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Élément UserCert EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef25a43bf13b1cfb1e4b03f78f5772567b3bfb92f1c31bb810da7882a4d3e1c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067229"
---
# <a name="usercert-eaptype-element"></a>Élément UserCert (EapType)

L’élément **UserCert (EapType)** fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

L’élément **UserCert** est défini par l’élément [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





