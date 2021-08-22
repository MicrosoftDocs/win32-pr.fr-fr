---
description: À propos des constantes de capteur
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: À propos des constantes de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cab8b5def4cdfa185a55dd993896fb5157563424b7753497413e5d7706465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890254"
---
# <a name="about-sensor-constants"></a>À propos des constantes de capteur

le capteur Windows et la plateforme d’emplacement utilisent des constantes de nombreuses façons. La plateforme définit différentes constantes que vous pouvez utiliser dans le code de votre pilote de capteur. Les fabricants de capteurs peuvent définir des constantes personnalisées. Vous pouvez trouver les définitions des constantes définies par la plateforme dans le fichier sensors. h. Pour plus d’informations sur les constantes de capteur définies par la plateforme, consultez [constantes](constants.md).

### <a name="sensor-and-data-organization"></a>Capteur et Organisation des données

La plateforme organise les capteurs et les données des manières suivantes.

-   Les catégories représentent des classes étendues de périphériques de capteur. Les catégories vous permettent de regrouper des capteurs susceptibles de fournir des types d’informations similaires ou qui sont liés autrement. Chaque catégorie est représentée par une constante **GUID** . Par exemple, les capteurs qui signalent des coordonnées de latitude et de longitude appartiennent à la catégorie de capteur d’emplacement. Cela est representented par la constante d’emplacement de la catégorie de capteur \_ \_ .
-   Les types de capteur représentent des genres spécifiques de capteurs. Chaque type de capteur s’intègre à une catégorie particulière. Deux capteurs de types différents peuvent appartenir à la même catégorie ou à des catégories différentes. Chaque type de capteur est représenté par une constante **GUID** . Par exemple, un capteur de système de positionnement global est identifié par la \_ constante GPS d’emplacement du type de capteur \_ \_ . Toutefois, un capteur qui fournit l’emplacement actuel à l’aide d’une adresse IP est identifié par la \_ constante de recherche d’emplacement du type de capteur \_ \_ . Toutefois, les deux capteurs appartiennent à la catégorie de capteur d’emplacement.
-   Les types de données représentent des types spécifiques d’informations que le capteur peut fournir. Les types de données de capteur peuvent contenir la valeur de mesure réelle, telle que l’altitude. informations sur les unités utilisées pour exprimer les données, telles que les compteurs ; et les points de référence pour les données, tels que le niveau Sea. Chaque type de données est représenté par une constante **PROPERTYKEY** . Par exemple, le type de données qui représente l’altitude au-dessus de la mer, en mètres, serait identifié par la \_ constante compteurs de données de capteur \_ \_ altitude \_ \_ .
-   Lors de la création de rapports de données, une valeur est considérée comme contenu dans un champ de données, et une collection de champs de données associés constitue un rapport de données. Les rapports de données sont regroupés à l’aide de l’interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) . Chaque rapport de données doit contenir au moins un champ de données valide et un horodatage qui identifie le moment où le rapport de données a été créé. Les horodatages sont représentés par la \_ constante horodateur du type de données de capteur \_ \_ .

### <a name="other-constants"></a>Autres constantes

Votre programme doit également utiliser d’autres constantes. Ces constantes sont les suivantes :

-   Propriétés du capteur, telles que la description de la propriété de capteur \_ \_ . En règle générale, ces constantes sont utilisées pour décrire un capteur. Certaines propriétés de capteur doivent être fournies par le capteur, certaines propriétés peuvent être définies par les applications clientes, et certaines doivent toujours retourner la même valeur à partir du capteur. La section de référence [**Propriétés du capteur**](sensor-properties.md) fournit ces informations pour chaque propriété.
-   Les constantes d’événement, telles que l’état des événements de capteur, \_ \_ \_ ont changé. Les constantes d’événement incluent des **GUID**, qui représentent des types d’événements, et **PROPERTYKEY** s, qui représentent des types de paramètres d’événement. Vous allez utiliser ces constantes pour les appels de méthode, tels que [**ISensor :: SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) et [**ISensor :: GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Constantes personnalisées

Les fabricants de capteurs peuvent définir des constantes personnalisées. Par exemple, un capteur peut appartenir à une catégorie non définie par la plateforme. Avant de pouvoir utiliser un capteur qui définit des constantes personnalisées, le fabricant du capteur doit publier les valeurs, par exemple en publiant un fichier d’en-tête. Pour plus d’informations, consultez la documentation fournie avec le capteur.

 

 
