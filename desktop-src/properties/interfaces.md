---
description: Cette section décrit les interfaces du système de propriétés Windows.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfaces (système de propriétés Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517870"
---
# <a name="interfaces-windows-property-system"></a>Interfaces (système de propriétés Windows)

Cette section décrit les interfaces du système de propriétés Windows.



| Rubrique                                                                                        | Contenu                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Expose une méthode qui encapsule une modification apportée à une propriété unique.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Expose des méthodes pour plusieurs opérations de modification qui peuvent être passées à [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation).                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Expose des méthodes qui énumèrent et récupèrent des détails sur la description de la propriété.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Expose des méthodes qui énumèrent et récupèrent des détails sur la description de la propriété.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Expose des méthodes pour obtenir les propriétés « Trier par » des colonnes pour un élément. Cette interface est utilisée par les objets d’interface utilisateur qui souhaitent récupérer les colonnes de tri principales ou secondaires pour une propriété donnée.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Expose des méthodes qui extraient des informations d’une collection de descriptions de propriétés présentées sous forme de liste.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Fournit une méthode qui récupère une interface [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Expose des informations relatives à la recherche pour une propriété. Les informations fournies par cette interface proviennent de l’élément [PropertyDescription](./propdesc-schema-propertydescription.md) Schema, [searchInfo](./propdesc-schema-searchinfo.md) pour une propriété donnée. Ces informations sont utilisées par l’indexeur de recherche Windows. La plupart des applications appelantes n’ont pas besoin d’appeler cette interface. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Expose des méthodes qui extraient des données à partir d’informations d’énumération. [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) donne accès aux éléments [enum](./propdesc-schema-enum.md) et [enumRange](./propdesc-schema-enumrange.md) du schéma de [propriété](./propdesc-schema-entry.md) par programmation au moment de l’exécution.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Expose des méthodes qui extraient des données à partir d’informations d’énumération. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) étend [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Expose des méthodes qui énumèrent les valeurs possibles d’une propriété.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Expose des méthodes pour énumérer, obtenir et définir des valeurs de propriété.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Expose des méthodes qui permettent à un gestionnaire de gérer différents États pour chaque propriété.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Expose une méthode qui détermine si une propriété peut être modifiée par l’utilisateur dans l’interface utilisateur.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Expose des méthodes pour récupérer un objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Expose des méthodes qui obtiennent des descriptions de propriété, inscrivent et désinscrit des schémas de propriété, énumèrent les descriptions de propriétés et les valeurs de propriété de format de façon stricte.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Les développeurs doivent utiliser [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) à la place.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés Windows](props.md)
</dt> <dt>

[Schéma de la description de propriété](property-description-schema.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> <dt>

[Fonctions](functions.md)
</dt> <dt>

[Structures](structures.md)
</dt> <dt>

[Constantes, énumérations et indicateurs](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
