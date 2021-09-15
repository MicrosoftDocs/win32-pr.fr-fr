---
description: Windows Périphériques portables prend en charge les propriétés d’association de réseau suivantes.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propriétés de l’Association réseau (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294387"
---
# <a name="network-association-properties"></a>Propriétés de l’Association réseau

Windows Périphériques portables prend en charge les propriétés d’association de réseau suivantes.



| Propriété                                                  | VarType                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ identificateurs de réseau hôte d’association de réseau wpd \_** | **VT \_ UI1 VT Vector \| \_** | Liste des identificateurs d’hôte EUI-64 valides pour cette association. Il s’agit d’un tableau d’octets qui contient un nombre entier d’adresses réseau physiques EUI-64. Ces valeurs EUI-64 sont les adresses réseau physiques disponibles sur l’hôte au moment de l’Association du réseau. Si l’ordinateur hôte possède des adresses réseau physiques MAC-48 (par défaut des réseaux IPv4), chaque adresse MAC-48 est encodée dans l’adresse EUI-64, car les deux moitiés de l’adresse MAC-48 sont séparées par FF-FF.<br/> |
| **\_Association de réseau wpd \_ \_ X509V3SEQUENCE**             | **VT \_ UI1 VT Vector \| \_** | Séquence des certificats X. 509 v3 à fournir pour l’authentification du serveur TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




