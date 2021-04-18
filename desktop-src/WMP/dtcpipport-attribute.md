---
title: Attribut DTCPIPPort
description: L’attribut DTCPIPPort est le numéro de port TCP (Transmission Control Protocol) de l’ordinateur ou du périphérique qui doit être contacté pour la transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Attribut DTCPIPPort lecteur Windows Media
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540719"
---
# <a name="dtcpipport-attribute"></a>Attribut DTCPIPPort

L’attribut **DTCPIPPort** est le numéro de port TCP (Transmission Control Protocol) de l’ordinateur ou du périphérique qui doit être contacté pour la Transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.

## <a name="applies-to"></a>S'applique à

-   [**Éléments audio**](audio-item-attributes.md)
-   [**Éléments de photo**](photo-item-attributes.md)
-   [**Éléments de sélection**](playlist-attributes-ref.md)
-   [**Éléments vidéo**](video-item-attributes.md)

## <a name="remarks"></a>Notes

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

 

 





