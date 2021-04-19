---
description: Appareils mobiles Windows prend en charge les propriétés de messagerie suivantes.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Propriétés de l’e-mail (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539704"
---
# <a name="email-properties"></a>Propriétés de l’e-mail

Appareils mobiles Windows prend en charge les propriétés de messagerie suivantes.



| Propriété                         | VarType        | Description                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ ligne CCI d’e-mail wpd \_**        | **\_LPWStr VT** | Destinataires CCI du message électronique. Les destinataires CCI reçoivent une copie du message, mais leurs noms ne sont pas affichés en tant que destinataires.   |
| **\_ \_ ligne CC de l’e-mail wpd \_**         | **\_LPWStr VT** | Destinataires CC du message électronique. Les destinataires CC reçoivent une copie du message électronique et leurs noms sont affichés en tant que destinataires. |
| **l' \_ E-mail wpd \_ contient des \_ pièces jointes** | **VT \_ bool**   | Valeur booléenne qui spécifie si ce message électronique contient des pièces jointes.                                                               |
| **l' \_ E-mail wpd \_ a \_ été \_ lu**  | **VT \_ bool**   | Valeur booléenne qui spécifie si ce message électronique a été lu.                                                                 |
| **heure de réception de l' \_ E-mail wpd \_ \_**   | **\_Date VT**   | Valeur qui spécifie à quel moment le message électronique a été reçu.                                                                              |
| **adresse d’expéditeur de l' \_ E-mail wpd \_ \_**  | **\_LPWStr VT** | Adresse électronique de l'expéditeur.                                                                                                         |
| **\_E-mail wpd \_ à la \_ ligne**         | **\_LPWStr VT** | Destinataires principaux du message électronique.                                                                                                |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




