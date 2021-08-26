---
description: Les qualificateurs de propriété spécifient des informations sur le compteur de performance mappé à la propriété.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Qualificateurs de propriété pour les classes de compteur de performance
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 105bd010704364dc3865b2e704b3daeaafdb29a772d4f3b3fe036b88da2d43cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996179"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a>Qualificateurs de propriété pour les classes de compteur de performance

Les qualificateurs de propriété spécifient des informations sur le compteur de performance mappé à la propriété.

-   [Qualificateurs de propriété pour les classes de performance brutes et mises en forme](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificateurs de propriété pour les classes de performance brutes](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Qualificateurs de propriété pour les classes de performance mises en forme](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [Comment interpréter les qualificateurs de propriété](#how-to-interpret-property-qualifiers)
-   [Rubriques connexes](#related-topics)

Le compteur de performance fait partie d’un objet de performance représenté par un compteur de performance de la [classe compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI. les qualificateurs spécifiques sont automatiquement attachés par le fournisseur WbemPerfClass aux classes et propriétés [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) dans le \\ cimv2 racine.

Ces informations s’appliquent à toutes les instances de la classe de performance. Certains qualificateurs avec des valeurs **booléennes** qui ont toujours la valeur false peuvent ne pas être présents sur des classes spécifiques.

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a>Qualificateurs de propriété pour les classes de performance brutes et mises en forme

La liste suivante répertorie les qualificateurs qui s’appliquent aux propriétés dans les classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ou [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)
</dt> <dd>

**sint32**

Valeur entière dans l’énumération de type de compteur, telle que définie dans Winperf. h ou Perflib. h. Le [**qualificateur de l’identificateur**](countertype-qualifier.md)de l’ordinateur indique la formule ou l’algorithme utilisé pour calculer la valeur affichée dans le moniteur système pour le compteur que la propriété représente.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**
</dt> <dd>

**string**

Nom du compteur de performance, tel que spécifié par le programme d’assistance des données de performances (PDH).

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**
</dt> <dd>

**sint32**

Non utilisé. Contient toujours la valeur 0.

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**
</dt> <dd>

**sint32**

Non utilisé. Contient toujours la valeur 0.

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a>Qualificateurs de propriété pour les classes de performance brutes

La liste suivante répertorie les qualificateurs qui s’appliquent à toutes les propriétés des classes dérivées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**
</dt> <dd>

**boolean**

Indique si cette propriété est le compteur par défaut à utiliser dans les zones de liste. Ce qualificateur a pour valeur par défaut **false** pour les compteurs de Performance version 6,0, car ils ne fournissent pas de données pour celui-ci. Pour plus d’informations, consultez [Compteurs de performances](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**
</dt> <dd>

**sint32**

Puissance de 10 à utiliser pour l’affichage du compteur. Pour zéro, la valeur maximale estimée est 10 ^ 0, ou 1.

</dd> <dt>

<span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)
</dt> <dd>

**sint32**

Niveau de connaissance de l’audience. Non utilisé. La valeur est toujours 100.

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a>Qualificateurs de propriété pour les classes de performance mises en forme

La liste suivante répertorie les qualificateurs qui s’appliquent à toutes les propriétés des classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**
</dt> <dd>

**string**

Type de formule utilisé pour produire le résultat. Chaque type de compteur utilise les autres qualificateurs de propriété pour calculer le résultat affiché comme valeur de la propriété actuelle. Les qualificateurs **Counter**, **PerfTimeStamp** et **PerfTimeFreq** sont mappés aux propriétés dans une classe brute qui fournit les données.

Pour plus d’informations, consultez la rubrique sur le [qualificateur](countertype-qualifier.md).

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**)**
</dt> <dd>

**string**

Nom d’une propriété requise dans la classe brute correspondante à utiliser comme valeur de compteur dans la formule de cuisson. La valeur doit être le nom de propriété de la propriété de source de données dans la classe brute correspondante.

</dd> <dt>

<span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**
</dt> <dd>

**string**

Nom d’une propriété dans une classe brute à utiliser comme fréquence dans la formule de cuisson. La valeur par défaut appropriée au niveau de la classe sera utilisée si ce qualificateur n’est pas présent pour la propriété. La fréquence représente les graduations par seconde de l’horodatage.

</dd> <dt>

<span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**
</dt> <dd>

**string**

Nom d’une propriété dans une classe brute à utiliser comme horodateur dans la formule de cuisson. La valeur par défaut appropriée au niveau de la classe est utilisée si ce qualificateur n’est pas présent pour la propriété. Un horodatage généré automatiquement peut introduire une erreur dans un calcul, car l’horodatage est une approximation et ne prend pas en compte la surcharge engendrée par le marshaling et la collecte de données réelle.

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a>Comment interpréter les qualificateurs de propriété

les propriétés dans les classes [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contiennent les données calculées fournies par le [Fournisseur de données de Performance mis en forme](formatted-performance-data-provider.md). La valeur de la propriété est le résultat final calculé. Les qualificateurs fournissent une recette.

Les qualificateurs **Counter** et **base** pointent vers les sources de données et **CookingType** spécifie la formule utilisée pour produire le résultat. L’horodateur et la fréquence d’échantillonnage proviennent également de la classe brute correspondante et sont nommés dans **PerfTimeStamp** et **PerfTimeFreq**.

Par exemple, l’une des classes mises en forme fournies par WMI, [**Win32 \_ PerfFormattedData \_ Perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contient une propriété nommée **AvgDiskBytesPerRead**. Le nom de la propriété dans la classe mise en forme doit être identique à la propriété de la classe brute. La propriété **AvgDiskBytesPerRead** a les qualificateurs suivants.

La liste suivante répertorie les qualificateurs de propriété disponibles pour les propriétés de toutes les classes dérivées de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).



| Qualificateur         | Valeur                     |
|-------------------|---------------------------|
| **CookingType**   | moyenne de performances \_ \_ en bloc       |
| **Compteur**       | AvgDiskBytesPerRead       |
| **PerfTimeStamp** | Horodateur \_ PerfTime       |
| **PerfTimeFreq**  | Fréquence \_ PerfTime       |
| **PerfIndex**     | 408                       |
| **HelpIndex**     | 409                       |
| **Base**          | \_Base AvgDiskBytesPerRead |



 

La propriété **AvgDiskBytesPerRead** indique le nombre moyen d’octets transférés à partir du disque pendant les opérations de lecture. La formule de la \_ moyenne des performances \_ est la suivante :

(Sample2-sample1)/(base sample2-base sample1)

L’opération de lecture est échantillonnée à la fréquence spécifiée par **PerfTimeFreq** avec la valeur **PerfTimeStamp** indiquant l’exemple le plus récent. Les données de compteur brutes en octets sont extraites de la propriété **AvgDiskBytesPerRead** de la classe [**\_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) . Le nombre de base de données d’opérations est extrait de la propriété de **\_ base AvgDiskBytesPerRead** dans cette même classe.

Pour plus d’informations, consultez [obtention de données de performances statistiques](obtaining-statistical-performance-data.md) et [analyse des données de performances](monitoring-performance-data.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Analyse des données de performances](monitoring-performance-data.md)
</dt> <dt>

[Qualificateurs spécifiques aux classes de performance WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Classes du compteur de performances](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accès aux classes de performance préinstallées par WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Tâches WMI : analyse des performances](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
