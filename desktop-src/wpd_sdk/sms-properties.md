---
description: Appareils mobiles Windows prend en charge les propriétés SMS suivantes.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propriétés de SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528461"
---
# <a name="sms-properties"></a>Propriétés SMS

Appareils mobiles Windows prend en charge les propriétés SMS suivantes.



| Propriété                   | VarType        | Description                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_encodage SMS wpd \_**     | **\_LPWStr VT** | Valeur qui spécifie la façon dont le pilote codera le message texte envoyé par le client. Il s’agit d’une propriété en lecture seule ; le client ne peut pas spécifier le type de codage utilisé par un appareil pour envoyer des messages. Ces valeurs dupliquent les valeurs énumérées des [**\_ \_ \_ types d’encodage SMS wpd**](wpd-sms-encoding-types.md) . |
| **\_ \_ charge utile max SMS pour wpd \_** | **VT \_ UI4**    | Nombre maximal d’octets qui peuvent être contenus dans un message.                                                                                                                                                                                                                                             |
| **\_fournisseur SMS \_ wpd**     | **\_LPWStr VT** | Nom du fournisseur de services.                                                                                                                                                                                                                                                                                |
| **\_ \_ délai d’expiration du SMS wpd**      | **VT \_ UI4**    | Nombre de millisecondes jusqu’à ce qu’un délai d’attente soit retourné.                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




