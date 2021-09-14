---
description: Windows Les appareils mobiles prennent en charge les propriétés diverses suivantes.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propriétés diverses (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234461"
---
# <a name="miscellaneous-properties"></a>Propriétés diverses

Windows Les appareils mobiles prennent en charge les propriétés diverses suivantes.



| Propriété                                       | VarType         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **l' \_ option de l’API WPD \_ utilise un \_ \_ \_ flux de données clair \_** | **VT \_ bool**    | Valeur booléenne qui spécifie si le flux de données créé pour le transfert de données est clair, c’est-à-dire que la DRM n’est pas impliquée. Les clients peuvent définir cette option en l’ajoutant aux propriétés d’objet passées à [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **\_version du service wpd \_**                      | **\_LPWStr VT**  | Chaîne qui spécifie la version d’implémentation d’un service d’appareil donné.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **\_types de contenu de dossier wpd \_ \_ \_ autorisés**       | **VT \_ inconnu** | Valeur qui spécifie les types d’objets qui peuvent être des enfants directs de ce dossier. Les dossiers enfants peuvent avoir des fonctionnalités différentes. Cette propriété est un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) contenant des \_ valeurs de CLSID VT qui spécifient des types d’objet autorisés.<br/> pour obtenir la liste des types d’objets définis par Windows appareils mobiles, consultez [configuration requise pour les objets](requirements-for-objects.md).<br/>                                         |
| **\_catégorie d' \_ objet \_ fonctionnel wpd**          | **\_CLSID VT**   | Valeur qui spécifie la catégorie fonctionnelle de l’objet.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_profils d' \_ informations de rendu wpd \_**      | **VT \_ inconnu** | Un [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) qui contient plusieurs interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , chacune contenant les paramètres de propriété d’un profil que l’objet prend en charge.                                                                                                                                                                                                                                            |
| **\_ \_ \_ \_ \_ nom complet de l’emplacement de l’indicateur d’objet wpd** | **\_LPWStr VT**  | Si un objet est un emplacement d’indication, cette propriété indique le nom spécifique à l’indicateur à afficher à l’utilisateur au lieu du nom de l’objet. Les pilotes peuvent spécifier des indications d’emplacement pour différents types d’objets. Il s’agit d’emplacements de stockage préférés pour les dossiers qui contiennent un type d’objet particulier. Un équivalent serait le dossier Mes images pour les fichiers image dans Windows. Si cette propriété n’existe pas, le nom de l' [ \_ \_ objet wpd](object-properties.md) est généralement utilisé à la place.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




