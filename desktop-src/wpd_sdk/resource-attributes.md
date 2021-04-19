---
description: Appareils mobiles Windows prend en charge les attributs de ressource suivants.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Attributs de ressource (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537640"
---
# <a name="resource-attributes"></a>Attributs de ressource

Appareils mobiles Windows prend en charge les attributs de ressource suivants. Ces attributs sont retournés par les méthodes suivantes :

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Attribut                                                  | VarType      | Description                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé**                  | **VT \_ bool** | Valeur booléenne qui spécifie si un client a l’autorisation de supprimer la ressource. Si elle est absente, elle est supposée avoir la valeur false.                |
| **l' \_ attribut de ressource wpd \_ \_ peut \_ lire**                    | **VT \_ bool** | Valeur booléenne qui spécifie si un client est autorisé à ouvrir la ressource pour l’accès en lecture. Si elle est absente, elle est supposée avoir la valeur false.  |
| **l' \_ attribut de ressource wpd \_ \_ peut \_ écrire**                   | **VT \_ bool** | Valeur booléenne qui spécifie si un client est autorisé à ouvrir la ressource pour l’accès en écriture. Si elle est absente, elle est supposée avoir la valeur false. |
| **\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd**  | **VT \_ UI4**  | Taille de mémoire tampon recommandée qu’un appelant doit utiliser pour les lectures mises en mémoire tampon à partir de la ressource.                                                  |
| **\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd** | **VT \_ UI4**  | Taille de mémoire tampon recommandée qu’un appelant doit utiliser pour les écritures mises en mémoire tampon sur la ressource.                                                   |
| **\_ \_ \_ taille totale de l’attribut de ressource wpd \_**                  | **\_UI8 VT**  | Taille totale des données de ressource, en octets.                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés**](properties-and-attributes.md)
</dt> </dl>

 

 




