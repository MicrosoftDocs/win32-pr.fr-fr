---
description: Identifie le nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Élément HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 1868be18dc7acf9d5146f987658feb006714fbcc3db35883007afd01c308609e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035827"
---
# <a name="homeprovidername-mbnprofile-element"></a>Élément HomeProviderName (MBNProfile)

L’élément **HomeProviderName (MBNProfile)** identifie le nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné.

Cet élément est facultatif et est défini par le service haut débit mobile pour une utilisation interne. Une application ne doit pas définir ce champ lors de la création ou de la mise à jour d’un profil.

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

L’élément **HomeProviderName** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Configuration requise



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

 

 




