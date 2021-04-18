---
description: Appareils mobiles Windows prend en charge les propriétés de données de la section suivante.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propriétés de l’attribut section (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528988"
---
# <a name="section-attribute-properties"></a>Propriétés de l’attribut de section

Appareils mobiles Windows prend en charge les propriétés de données de la section suivante.



| Propriété                                             | VarType         | Description                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **longueur des données de la \_ section wpd \_ \_**                       | **\_UI8 VT**     | Spécifie la longueur de l’objet référencé.                                                                                                                                                                                                                                                                                              |
| **décalage des données de la \_ section wpd \_ \_**                       | **\_UI8 VT**     | Spécifie l’offset de base zéro des données pour l’objet référencé.                                                                                                                                                                                                                                                                      |
| **\_ressource d' \_ objet de référence des données \_ \_ de la section wpd \_** | **VT \_ inconnu** | [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenant une valeur unique qui spécifie la clé d’une ressource donnée. Cette ressource est l’objet référencé par la \_ section offset de données de la section wpd \_ et la \_ longueur des données de la \_ section wpd \_ \_ .<br/> Si cette propriété n’existe pas, \_ la \_ valeur par défaut de la ressource wpd est supposée.<br/> |
| **unités de données de la \_ section wpd \_ \_**                        | **VT \_ UI4**     | Spécifie les unités utilisées pour ce décalage, par exemple, les octets, les millisecondes, etc. Les valeurs possibles de cette propriété sont définies dans l’énumération des valeurs d’unités de données de la **\_ section \_ \_ \_ wpd** dans le fichier PortableDevice. h.<br/> Si aucune unité n’est spécifiée, les octets sont supposés.<br/>                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




