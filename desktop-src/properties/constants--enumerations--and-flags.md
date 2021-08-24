---
description: cette section décrit les Windows constantes, énumérations et indicateurs du système de propriétés.
ms.assetid: ff735b9c-e444-4e6f-8e80-0b2a5d770386
title: constantes, énumérations et indicateurs (Windows système de propriétés)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e39d357ae741ae49c4fa98c886e8c08b3594a2ea3a7e4e045def96abe8c2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718208"
---
# <a name="constants-enumerations-and-flags"></a>Constantes, énumérations et indicateurs

cette section décrit les Windows constantes, énumérations et indicateurs du système de propriétés.



| Rubrique                                                                              | Contenu                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETPROPERTYSTOREFLAGS**](/windows/desktop/api/Propsys/ne-propsys-getpropertystoreflags)                             | Indique les indicateurs qui modifient l’objet de la Banque de propriétés récupéré par les méthodes qui créent une banque de propriétés, par exemple [**IShellItem2 :: GetPropertyStore**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellitem2-getpropertystore) ou [**IPropertyStoreFactory :: GetPropertyStore**](/windows/win32/api/propsys/nf-propsys-ipropertystorefactory-getpropertystore).<br/>                                                                                        |
| [**PDOPSTATUS**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-pdopstatus)                                                 | Fournit des indicateurs d’état d’opération.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**\_indicateurs pKa**](/windows/win32/api/propsys/ne-propsys-pka_flags)                                                  | Décrit le comportement du tableau de modification de propriété.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_type d’agrégation PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_aggregation_type)                 | Décrit comment les valeurs de propriété s’affichent lorsque plusieurs éléments sont sélectionnés. Pour une propriété particulière, \_ le type d’agrégation PROPDESC \_ décrit la manière dont la propriété doit être affichée lorsque plusieurs éléments qui ont une valeur pour la propriété sont sélectionnés, par exemple si les valeurs doivent être additionnées ou calculées en moyenne, ou simplement affichées avec la chaîne « valeurs multiples » par défaut.<br/> |
| [**TYPE de PROPDESC \_ COLUMNINDEX \_**](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)                 | Indique si ou comment une propriété peut être indexée.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**\_type de condition PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_condition_type)                     | décrit le type de condition à utiliser lors de l’affichage de la propriété dans l’interface utilisateur du générateur de requêtes dans Windows Vista, mais pas dans Windows 7 et versions ultérieures.<br/>                                                                                                                                                                                                                                      |
| [**PROPDESC \_ ENUMFILTER**](/windows/win32/api/propsys/ne-propsys-propdesc_enumfilter)                              | Décrit la liste filtrée des descriptions de propriété retournées.<br/>                                                                                                                                                                                                                                                                                                          |
| [**\_indicateurs de format PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_format_flags)                         | Utilisé par les fonctions d’assistance de description de propriété, telles que [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay), pour indiquer le format d’une chaîne de propriété.<br/>                                                                                                                                                                                                                         |
| [**\_type RELATIVEDESCRIPTION \_ PROPDESC**](/windows/win32/api/propsys/ne-propsys-propdesc_relativedescription_type) | Décrit le type de description relative pour une description de propriété, tel que déterminé par l’attribut *relativeDescriptionType* de l’élément [displayInfo](./propdesc-schema-displayinfo.md) .<br/>                                                                                                                                                                                   |
| [**PROPDESC \_ SEARCHINFO, \_ indicateurs**](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)                 | détermine si et comment une propriété est indexée par Windows recherche.<br/>                                                                                                                                                                                                                                                                                                             |
| [**\_indicateurs de type PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_type_flags)                             | Décrit les attributs de l’élément [TypeInfo](./propdesc-schema-typeinfo.md) dans le fichier. propDesc de la propriété.<br/>                                                                                                                                                                                                                                                                |
| [**\_indicateurs d’affichage PROPDESC \_**](/windows/win32/api/propsys/ne-propsys-propdesc_view_flags)                             | Ces indicateurs décrivent les propriétés dans les chaînes de liste de description de propriété.<br/>                                                                                                                                                                                                                                                                                                           |
| [**\_indicateurs PROPERTYUI**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_propertyui_flags)                                    | Spécifie les fonctionnalités de propriété.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**\_unité de comparaison PROPVAR \_**](/windows/win32/api/propvarutil/ne-propvarutil-propvar_compare_unit)                           | Ces indicateurs sont associés à certaines comparaisons de structures [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .<br/>                                                                                                                                                                                                                                                                               |
| [**État du PSC \_**](/windows/win32/api/propsys/ne-propsys-psc_state)                                                  | Spécifie l’état d’une propriété. Elles sont définies manuellement par le code qui héberge le cache de la Banque de propriétés en mémoire.<br/>                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés Windows](props.md)
</dt> <dt>

[Schéma de la description de propriété](property-description-schema.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> <dt>

[Interfaces](interfaces.md)
</dt> <dt>

[Fonctions](functions.md)
</dt> <dt>

[Structures](structures.md)
</dt> </dl>

 

 
