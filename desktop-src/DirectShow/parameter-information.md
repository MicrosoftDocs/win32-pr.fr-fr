---
description: Informations sur les paramètres
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: Informations sur les paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312310"
---
# <a name="parameter-information"></a>Informations sur les paramètres

La méthode [**IMediaParamInfo :: GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) retourne une structure [**MP \_ ParamInfo et**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) qui décrit un paramètre. Cette structure contient les informations suivantes :

-   Le membre **mpType** indique le type de données de la valeur de paramètre. Pour des performances optimales, tous les paramètres sont implémentés en tant que valeurs à virgule flottante 32 bits. L’énumération de [**\_ type MP**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) définit s’il faut interpréter la valeur comme un entier, une valeur à virgule flottante, une valeur booléenne ou une énumération (série d’entiers).
-   Le membre **mopCaps** indique les courbes prises en charge par ce paramètre. Si le type de données est booléen ou énumération, la seule courbe que le paramètre peut prendre en charge est « sauter ».
-   Les membres **mpdMinValue** et **mpdMaxValue** définissent les valeurs minimale et maximale de ce paramètre. Toutes les courbes de ce paramètre doivent être comprises dans cette plage.
-   Le membre **mpdNeutralValue** est la valeur par défaut du paramètre.
-   Le membre **szLabel** est le nom du paramètre et le membre **szUnitText** est le nom de l’unité de mesure du paramètre. Les exemples peuvent inclure « volume » et « décibels » ou « Frequency » et « kHz ». Les deux chaînes sont en anglais et ne sont jamais localisées. la DMO peut fournir des versions localisées par le biais de la méthode [**IMediaParamInfo :: GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) .

Les informations de chaque paramètre restent fixes tout au long de la durée de vie de la DMO. Par conséquent, le client peut interroger ces informations une seule fois, puis les mettre en cache.

**Formats d’heure**

le client doit horodatager les données d’entrée, afin que le DMO puisse calculer les valeurs de paramètres correspondantes. Par défaut, les horodatages représentent les unités de 100 nanosecondes, également appelées *temps de référence*. toutefois, cette unité de temps n’est pas pratique pour chaque application. par conséquent, un DMO a la possibilité de prendre en charge d’autres formats d’heure. Les formats d’heure sont identifiés par GUID.



| **GUID**              | Description                   |
|-----------------------|-------------------------------|
| \_référence de temps GUID \_ | Temps de référence                |
| durée du GUID \_ \_     | Remarque relative aux parties par trimestre (PPQN) |
| \_exemples d’heure GUID \_   | Échantillons par seconde            |



 

Des tiers sont encouragés à définir leurs propres formats d’heure en fonction des besoins. Toutefois, tous les DMOs doivent prendre en charge le temps de référence. Cela fournit une ligne de base standard que tout le monde peut utiliser. pour déterminer le nombre de formats d’heure pris en charge par un DMO, appelez la méthode [**IMediaParamInfo :: GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) . Pour énumérer les formats pris en charge, appelez la méthode [**IMediaParamInfo :: GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) .

Pour définir le format d’heure, appelez [**IMediaParams :: SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat). Cette méthode spécifie le GUID du format d’heure et les *données d’heure*, qui est le nombre d’unités par cycle d’horloge. Par exemple, si le format d’heure est des échantillons par seconde et que les données d’heure sont 32, une valeur d’horodatage de 10 correspond à 320 échantillons.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres de média](media-parameters.md)
</dt> </dl>

 

 



