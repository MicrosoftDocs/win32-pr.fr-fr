---
title: Sérialisation du jeu de propriétés
description: Il existe deux versions du format de sérialisation du jeu de propriétés.
ms.assetid: 10544118-5e80-47e2-b75b-c1a43be15b2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f340b31252bfc3d99f72746e8ae791f313498c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989152"
---
# <a name="property-set-serialization"></a>Sérialisation du jeu de propriétés

Il existe deux versions du format de sérialisation du jeu de propriétés. La spécification d’origine décrit la version 0 du format. Pour plus d’informations, consultez [format version](format-version.md) . La version 1 étend la version d’origine. Tous les jeux de propriétés de la version 0 sont valides en tant que jeux de propriétés version 1. Le champ **version de format** dans l’en-tête d’un jeu de propriétés sérialisées indique la version.

Les éléments suivants identifient les différences entre les formats de sérialisation des jeux de propriétés version 0 et version 1.

-   Prise en charge des nouvelles valeurs **VarType** . Pour plus d’informations sur les valeurs **VarType** et leur utilisation, consultez la rubrique [IDispatch Data types and structures]( /previous-versions/ms221600(v=vs.100)) et la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

    Les valeurs **VarType** suivantes ne sont pas prises en charge dans les jeux de propriétés de la version 0, mais sont prises en charge dans la version 1 :

    VT_I1

    VT_VECTOR \| VT_I1

    VT_INT

    VT_UINT

    VT_DECIMAL

    En outre, les SAFEARRAY peuvent être sérialisés dans un jeu de propriétés. La présence d’un SafeArray est indiquée par le bit de VT_ARRAY combiné, à l’aide d’une opération **ou** , avec les éléments de tableau dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Par exemple, un SafeArray d’entiers signés de 4 octets a un type de VT_ARRAY \| VT_I4.

    Les types d’éléments suivants sont valides pour un SafeArray dans un jeu de propriétés sérialisé :

    | <!--tabular list: col headers unnecessary-->  ||||
    |-------------|----------|-------------|-----------|
    | VT_I1       | VT_UI1   | VT_I2       | VT_UI2    |
    | VT_I4       | VT_UI4   | VT_INT      | VT_UINT   |
    | VT_R4       | VT_R8    | VT_CY       | VT_DATE   |
    | VT_BSTR     | VT_BOOL  | VT_DECIMAL  | VT_ERROR  |
    | VT_VARIANT  |          |             |           |
    |             |          |             |           |

    Lorsque le type de données VT_VARIANT est spécifié, il indique que le SafeArray lui-même contient des structures [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Les types de ces éléments doivent provenir de la liste précédente, sauf qu’ils ne peuvent pas contenir de types de VT_VARIANT imbriqués.
    
    Notez que les implémentations de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) doivent être en mesure de récupérer correctement en renvoyant une erreur lorsqu’un nouveau type est rencontré ; par exemple, les types VARENUM.

-   Noms des propriétés sensibles à la casse. Les noms de propriétés, par exemple ceux qui sont spécifiés dans la méthode [**IPropertyStorage :: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames) , ne respectent pas la casse dans les jeux de propriétés de la version 0. Dans les jeux de propriétés de la version 1, les noms de propriété peuvent être sensibles à la casse selon la valeur de la nouvelle propriété de comportement.

    La propriété Behavior est l' [ID de propriété 0x80000003](/windows/desktop/Stg/reserved-property-identifiers) avec un type de VT_UI4. Si le bit le plus bas de cette valeur est défini, les noms des jeux de propriétés respectent la casse. Définissez l’indicateur PROPSETFLAG_CASE_SENSITIVE dans le paramètre *grfFlags* de la méthode [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) pour spécifier un jeu de propriétés respectant la casse.

-   Noms de propriétés de type long. Les noms de propriété pour les jeux de propriétés de la version 0 doivent être inférieurs ou égaux à 256 caractères, y compris la marque de fin de chaîne, pour les jeux de propriétés dans la page de codes Unicode. Si elle ne figure pas dans la page de codes Unicode, elle doit être inférieure à 256 octets. En revanche, les jeux de propriétés de la version 1 peuvent avoir des noms de propriété de longueur illimitée, bien qu’ils soient toujours limités par la limite de taille du jeu de propriétés global de 256 kilo-octets (Ko).

Il est recommandé que les implémentations de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) créent et maintiennent les jeux de propriétés de la version 0 par défaut. Si un appelant demande par la suite une fonctionnalité spécifique au format version 1, uniquement si la version du jeu de propriétés doit être mise à jour. Par exemple, si une propriété de type VT_ARRAY est écrite ou si un nom de propriété long est écrit, l’implémentation doit mettre à jour le format du jeu de propriétés à la version 1. Une exception à cette règle se produit si la PROPSETFLAG_CASE_SENSITIVE valeur d’énumération est spécifiée dans l’appel à [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Dans ce cas, le jeu de propriétés doit être créé en tant que jeu de propriétés de la version 1.

 

 
