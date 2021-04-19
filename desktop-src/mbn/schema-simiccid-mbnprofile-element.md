---
description: Identifie le numéro d’identification SIM pour les appareils GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Élément SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532085"
---
# <a name="simiccid-mbnprofile-element"></a>Élément SimIccID (MBNProfile)

L’élément **SimIccID (MBNProfile)** identifie le numéro d’identification SIM pour les appareils GSM.

Cet élément est facultatif et est défini par le service haut débit mobile pour une utilisation interne. Une application ne doit pas définir ce champ lors de la création ou de la mise à jour d’un profil.

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

L’élément **SimIccID** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




