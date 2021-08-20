---
description: Identifie l’identificateur unique du profil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Élément abonné (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: 42290b0a80e85b2fdd1c794aced78571e939010b0e260bf1bdeba15f221cc103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065883"
---
# <a name="subscriberid-mbnprofile-element"></a>Élément abonné (MBNProfile)

L’élément **abonné (MBNProfile)** identifie l’identificateur unique du profil.

Pour un réseau GSM, il doit contenir le IMSI (identité de l’abonné mobile international) de la carte SIM et des appareils CDMA. il doit contenir la valeur minimale (numéro d’identification mobile) de l’appareil.

L’élément est une chaîne numérique d’une longueur maximale de 15 chiffres.

L’élément est obligatoire.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

L’élément **abonné** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




