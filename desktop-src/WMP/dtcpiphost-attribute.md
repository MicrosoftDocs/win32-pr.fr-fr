---
title: Attribut DTCPIPHost
description: l’attribut DTCPIPHost est le nom ou l’adresse IP de l’ordinateur ou du périphérique qui doit être contacté pour la Exchange de la clé authentifiée protection du contenu sur Internet Protocol (acé) pour l’élément multimédia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Lecteur Windows Media de l’attribut DTCPIPHost
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88eaa85b756a46b1333db2e5eabda9cbaf86a702f5ae9c8225d6f6d8928e2d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996949"
---
# <a name="dtcpiphost-attribute"></a>Attribut DTCPIPHost

l’attribut **DTCPIPHost** est le nom ou l’adresse IP de l’ordinateur ou du périphérique qui doit être contacté pour la Exchange de la clé authentifiée protection du contenu sur Internet Protocol (acé) pour l’élément multimédia.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Remarques

Si cet attribut est disponible, l’élément multimédia est protégé à l’aide de DTCP-IP.

Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel. Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé. Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 12<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





