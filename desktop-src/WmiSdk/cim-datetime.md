---
description: Vous pouvez accéder à toutes les dates et heures du Common Information Model (CIM) dans WMI en utilisant l’un des deux formats de longueur fixe spécifiques à WMI et CIM. Dans les scripts, utilisez l’objet SWbemDateTime pour les convertir en dates et heures régulières.
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520121"
---
# <a name="cim_datetime"></a>\_DateTime CIM

Vous pouvez accéder à toutes les dates et heures du [*Common Information Model (CIM)*](gloss-c.md) dans WMI en utilisant l’un des deux formats de longueur fixe spécifiques à WMI et CIM. Dans les scripts, utilisez l’objet [**SWbemDateTime**](swbemdatetime.md) pour les convertir en dates et heures régulières.

Les sections suivantes décrivent l’utilisation des formats de date et d’heure WMI.

## <a name="format"></a>Format

Le tableau suivant répertorie les deux formats de date et d’heure utilisés par WMI.



| Format                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Date/heure](datetime.md)<br/> *AAAAMMJJHHMMSS. mmmmmmsUUU*<br/>                             | Format dans lequel sont stockées les valeurs [**DateTime**](datetime.md) CIM. Ce format est indépendant des paramètres régionaux, ce qui vous permet d’écrire un script qui s’exécute sur n’importe quel ordinateur. Vous devez utiliser ce format pour définir une date et une heure en [*format MOF (MOF)*](gloss-m.md)ou lors de l’écriture dans une instance à l’aide [de l’API com pour WMI](com-api-for-wmi.md) ou [de l’API de script pour WMI](scripting-api-for-wmi.md). Pour plus d’informations, consultez [modification d’une propriété d’instance](modifying-an-instance-property.md). |
| Format valide uniquement dans les requêtes Langage de requêtes WMI (WQL) (WQL).<br/> *AAAA-MM-JJ HH : MM : SS : MMM*<br/> | Ce format peut être utilisé dans les scripts qui utilisent les méthodes [**SWbemDateTime**](swbemdatetime.md) . Pour plus d’informations, consultez [interrogation de WMI](querying-wmi.md) ou [interrogation avec WQL](querying-with-wql.md). Ce format n’est pas indépendant des paramètres régionaux. L’ordre de l’année, du mois et du jour dépend du paramètre de format régional et de langue de la session utilisateur. Par exemple, alors que la valeur par défaut pour États-Unis anglais est « mm-jj-aaaa hh : mm : SS : MMM », le format de la plupart des autres pays ou régions est « yyyy-mm-jj hh : mm : SS : mmm ».       |



 

Le tableau suivant répertorie les champs dans les formats.



| Champ    | Description                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *yyyy*   | Année à quatre chiffres (0000 à 9999). Votre implémentation peut restreindre la plage prise en charge. Par exemple, une implémentation peut prendre en charge uniquement les années 1980 à 2099.                                                                         |
| *mm*     | Mois à deux chiffres (01 à 12).                                                                                                                                                                                                                |
| *dd*     | Jour à deux chiffres du mois (01 à 31). Cette valeur doit être appropriée pour le mois. Par exemple, le 31 février n’est pas valide. Toutefois, votre implémentation n’a pas besoin de vérifier la validité des données.                                            |
| *HH*     | Heure à deux chiffres de la journée à l’aide de l’horloge de 24 heures (00 à 23).                                                                                                                                                                              |
| *MM*     | Minutes à deux chiffres dans l’heure (00 à 59).                                                                                                                                                                                                   |
| *SS*     | Nombre de secondes à deux chiffres dans la minute (00 à 59).                                                                                                                                                                                      |
| *mmmmmm* | Nombre de microsecondes de six chiffres dans le deuxième (000000 à 999999). Votre implémentation n’a pas besoin de prendre en charge l’évaluation à l’aide de ce champ. Toutefois, ce champ doit toujours être présent pour préserver la nature de longueur fixe de la chaîne. |
| *mmm*    | Nombre de millisecondes à trois chiffres dans la minute (de 000 à 999).                                                                                                                                                                             |
| *s*      | Signe plus (+) ou moins (-) pour indiquer un décalage positif ou négatif par rapport aux heures universelles (UTC, Universal Time Coordinated).                                                                                                                               |
| *UUU*    | Décalage à trois chiffres indiquant le nombre de minutes pendant lequel le fuseau horaire d’origine s’écarte de l’heure UTC. Pour WMI, il est recommandé, mais pas obligatoire, de convertir les heures en heure GMT (décalage UTC de zéro).                                              |



 

Vous devez entrer tous les champs avec la longueur indiquée, en utilisant des zéros non significatifs comme il convient pour le type. Toutefois, utilisez des astérisques pour indiquer les champs inutilisés ou en tant que valeur générique. Vous pouvez utiliser un astérisque ( \* ) partout, à l’exception de la clause **Where** d’une requête. Par exemple, une date et une heure avec une année non spécifiée peuvent se produire dans n’importe quelle année. Si vous souhaitez conserver un champ non spécifié, vous devez remplacer le champ entier par des astérisques.

Les exemples suivants décrivent les utilisations valides et non valides des astérisques :

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (légal)
-   1998-04-16 \* \* \* \* \* \* : \* \* \* (non conforme)
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (non conforme)
-   199 \* -04-16 \* \* \* \* \* \* : \* \* \* (non conforme)

Si une valeur DateTime est utilisée pour représenter un point spécifique dans le temps, tous ses champs doivent inclure des données. S’il est utilisé pour représenter une plage de temps, seuls les champs nécessaires pour transmettre la durée doivent inclure des données.

L’exemple suivant décrit « April First » : une date relative à une année non spécifiée, mais toujours un point défini si le niveau de détail de mesure est d’un jour.

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* : \* \* \* (non conforme)

## <a name="setting-utc-offset-and-gmt"></a>Définition du décalage UTC et de l’heure GMT

Les exemples suivants décrivent comment vous pouvez définir une heure sans fuseau horaire en plaçant des astérisques dans le champ UUU après le signe plus ou moins :

-   19980401135809.000000 +\*\*\*
-   19980401135809,000000-\*\*\*
-   1998-04-01 13:58:09 : \* \* \* (non conforme)

Une application interprète une référence de date et d’heure non zone à un Chronometer abstrait local au sein du système d’exploitation en cours d’exécution. Par exemple, les ordinateurs portables peuvent avoir des horloges internes dont les paramètres peuvent ou non correspondre au fuseau horaire géographique. Vous pouvez interpréter le temps non-zone en substituant le fuseau horaire de la source de temps abstraite actuelle au lieu du fuseau horaire local.

Vous devez accorder une attention particulière à la signification du décalage UTC avec les dates et les heures dans les requêtes. En général, les comparaisons d’équivalence, supérieur à ou inférieur à fonctionnent entre deux dates et heures si les dates et les heures utilisent le même décalage UTC. Lorsque vous traitez des dates et heures qui se produisent avec différents décalages de fuseau horaire, vous devez d’abord convertir les dates et heures en heure GMT.

Les requêtes qui impliquent des dates et heures relatives avec des astérisques dans un ou plusieurs sous-champs sont significatives pour WMI uniquement lorsqu’elles sont comparées à des fins d’équivalence. En outre, WMI n’autorise pas l’utilisation des astérisques comme caractères génériques. Au lieu de cela, WMI compare les dates et les heures relatives à un caractère pour caractère.

Les exemples suivants décrivent deux dates qu’une requête WMI n’est pas prise en compte :

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>Conversion au format de date FILETIME ou VT \_

Le format [**DateTime**](datetime.md) CIM est utilisé uniquement dans WMI. Vous pouvez effectuer une conversion vers et à partir du format WMI et du \_ format de date FILETIME ou VT en appelant les méthodes de l’objet de script [**SWbemDateTime**](swbemdatetime.md) . Une structure **DateTime** [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) est une valeur 64 bits qui est utilisée par les systèmes d’exploitation Windows 32 bits. Le \_ format de date VT est une valeur DateTime de variante Automation utilisée par Visual Basic et ActiveX. Le tableau suivant répertorie les méthodes de conversion.



| Méthode                                                         | Description                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime. GetFileTime**](swbemdatetime-getfiletime.md) | Obtient une valeur [**DateTime**](datetime.md) au format [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .                |
| [**SWbemDateTime. getVarDate,**](swbemdatetime-getvardate.md)   | Obtient une valeur [**DateTime**](datetime.md) au \_ format de date VT.                                         |
| [**SWbemDateTime.SetFileTime**](swbemdatetime-setvardate.md)  | Définit une propriété [**DateTime**](datetime.md) à l’aide d’une date [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) comme entrée. |
| [**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)   | Définit une propriété [**DateTime**](datetime.md) à l’aide d’une date de \_ Date VT comme entrée.                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de date et d’heure](date-and-time-format.md)
</dt> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dt>

[Tâches WMI : dates et heures](wmi-tasks--dates-and-times.md)
</dt> <dt>

[Format d’intervalle](interval-format.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServicesEx. put**](swbemservicesex-put.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices ::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

