---
title: Gestion des propriétés
description: Chaque propriété se compose d’un identificateur de propriété (unique dans son jeu de propriétés), d’une balise de type Variant (VT ou VarType) qui représente le type d’une valeur et de la valeur elle-même.
ms.assetid: d220ecb4-b014-4ac9-a636-9a493187cc87
keywords:
- structured Stockage Strctd Stg, utilisation, gestion des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a792b734ae66c2f5077f4e3a98e6c0f3f53f97a482d7e4ade46de574c03153d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126399"
---
# <a name="managing-properties"></a>Gestion des propriétés

Chaque propriété se compose d’un *identificateur de propriété* (unique dans son jeu de propriétés), d’une *balise de type Variant (VT ou VarType)* qui représente le type d’une valeur et de la *valeur* elle-même. La balise de type Variant décrit la représentation des données dans la valeur. En outre, une propriété peut également se voir attribuer un *nom de chaîne* qui peut être utilisé pour identifier la propriété, plutôt que d’utiliser l’identificateur de propriété numérique (ID) requis. Pour créer et gérer des propriétés, COM définit l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .

L’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) comprend des méthodes permettant de lire et d’écrire des tableaux de propriétés ou de noms de propriétés. L’interface comprend des méthodes [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) et [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) qui sont similaires aux méthodes [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) du même nom. Il existe des méthodes utilitaires qui vous permettent de définir l’identificateur de classe (CLSID) du jeu de propriétés, de définir les heures associées à l’ensemble et d’obtenir des statistiques sur le jeu de propriétés. Enfin, la méthode [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) crée un énumérateur et retourne un pointeur vers son interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) . Vous pouvez appeler les méthodes de cette interface pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) sur votre objet, ce qui fournit des informations sur toutes les propriétés dans le jeu de propriétés actuel.

Voici un exemple de la façon dont les propriétés sont représentées. Si une propriété spécifique dans un jeu de propriétés contient le nom scientifique d’un animal, ce nom peut être stocké sous la forme d’une chaîne se terminant par zéro. Stocké avec le nom est un indicateur de type pour indiquer que la valeur est une chaîne se terminant par zéro. Ces propriétés peuvent avoir les caractéristiques suivantes :



| ID de propriété | Identificateur de chaîne | Indicateur de type | Valeur représentée              |
|-------------|-------------------|----------------|--------------------------------|
| 02          | PID \_ ANIMALNAME   | \_LPWStr VT     | Chaîne Unicode se terminant par zéro |
| 03          | PID \_ LEGCOUNT     | VT \_ I2         | WORD                           |



 

Toute application qui reconnaît le format du jeu de propriétés, en l’identifiant par son identificateur de format (FMTID), peut examiner la propriété avec un identificateur PID \_ ANIMALNAME, déterminer qu’il s’agit d’une chaîne se terminant par zéro, et lire et écrire la valeur. Bien que l’application puisse appeler [**IPropertyStorage :: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) pour lire tout ou partie d’un jeu de propriétés (ayant obtenu d’abord un pointeur), l’application doit savoir comment interpréter le jeu de propriétés.

Une valeur de propriété est passée via des interfaces de propriété en tant qu’instance du type [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).

Il est important de faire la distinction entre ces propriétés stockées (persistantes) et les propriétés d’exécution. Les constantes de valeur de type Variant portent des noms commençant par VT \_ . toutefois, l’ensemble des PROPVARIANTs valides n’est pas entièrement équivalent à l’ensemble des variantes utilisées dans l’automatisation et les contrôles de ActiveX.

La seule différence entre les deux structures est l’ensemble autorisé de \_ balises VT (variant type/VarType) dans chaque. Lorsqu’un type de propriété donné peut être utilisé à la fois dans un VARIANT et un PROPVARIANT, la balise de type (la \_ valeur VT) a toujours une valeur identique. En outre, pour une valeur VT donnée \_ , la représentation en mémoire utilisée dans les variantes et PROPVARIANTs est identique. Pris ensemble, cette approche permet au système de type d’intercepter les balises de type non autorisées, tout en permettant à un client compétent d’implémenter une conversion de pointeur quand cela est approprié.

pour plus d’informations, consultez la section suivante, [Stockage considérations relatives](property-storage-considerations.md)à la propriété.

 

 