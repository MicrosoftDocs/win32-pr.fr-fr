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
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751292"
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
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
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

 

 




