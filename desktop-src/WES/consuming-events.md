---
title: consommation d’événements (journal des événements Windows)
description: Vous pouvez consommer des événements à partir de canaux ou de fichiers journaux.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131f0f3b02485c3c838e9180ea1daaebb4121b8846e5a124f36cfdb6bf377f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620379"
---
# <a name="consuming-events-windows-event-log"></a>consommation d’événements (journal des événements Windows)

Vous pouvez consommer des événements à partir de canaux ou de fichiers journaux. Pour consommer des événements, vous pouvez utiliser tous les événements ou vous pouvez spécifier une expression XPath qui identifie les événements que vous souhaitez utiliser. Pour déterminer les éléments et les attributs d’un événement que vous pouvez utiliser dans votre expression XPath, consultez [schéma d’événement](eventschema-schema.md).

Windows Le journal des événements prend en charge un sous-ensemble de XPath 1,0. Pour plus d’informations sur les limitations, consultez [limitations de XPath 1,0](#xpath-10-limitations).

Les exemples suivants illustrent des expressions XPath simples.


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



Vous pouvez utiliser les expressions XPath directement lors de l’appel des fonctions [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , ou vous pouvez utiliser une requête XML structurée qui contient l’expression XPath. Pour les requêtes simples qui interrogent des événements à partir d’une seule source, l’utilisation d’une expression XPath est correcte. Si l’expression XPath est une expression composée qui contient plus de 20 expressions ou si vous interrogez des événements à partir de plusieurs sources, vous devez utiliser une requête XML structurée. Pour plus d’informations sur les éléments d’une requête XML structurée, consultez [schéma de requête](queryschema-schema.md).

Une requête structurée identifie la source des événements et un ou plusieurs sélecteurs ou suppressions. Un sélecteur contient des expressions XPath qui sélectionnent les événements de la source et un suppresseur contient une expression XPath qui empêche la sélection des événements. Vous pouvez sélectionner des événements à partir de plusieurs sources. Si un sélecteur et un suppresseur identifient le même événement, l’événement n’est pas inclus dans le résultat.

L’exemple suivant montre une requête XML structurée qui spécifie un ensemble de sélecteurs et de suppressions.


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



Le jeu de résultats de la requête ne contient pas d’instantané des événements au moment de la requête. Au lieu de cela, le jeu de résultats comprend les événements au moment de la requête et contient également tous les nouveaux événements qui sont générés et qui correspondent aux critères de la requête lors de l’énumération des résultats.

> [!Note]  
> L’ordre des événements est préservé pour les événements écrits par le même thread. Toutefois, il est possible que les événements écrits par des threads distincts sur différents processeurs d’un ordinateur à plusieurs processeurs apparaissent dans le désordre.

 

Pour plus d’informations sur l’utilisation des événements, consultez les rubriques suivantes :

-   [Interrogation des événements](querying-for-events.md)
-   [Abonnement à des événements](subscribing-to-events.md)
-   [Événements de rendu](rendering-events.md)
-   [Mise en forme des messages d’événement](formatting-event-messages.md)
-   [Événements de signets](bookmarking-events.md)

Les outils de l’utilisateur final standard pour l’événement de consommation sont les suivants :

-   [Observateur d’événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   applet de commande Windows PowerShell [WinEvent](/previous-versions//dd367894(v=technet.10))
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitations de XPath 1,0

Windows Le journal des événements prend en charge un sous-ensemble de XPath 1,0. La restriction principale est que seuls les éléments XML qui représentent des événements peuvent être sélectionnés par un sélecteur d’événements. Une requête XPath qui ne sélectionne pas d’événement n’est pas valide. Tous les chemins de sélecteur valides commencent par \* ou « Event ». Tous les chemins d’accès d’emplacement fonctionnent sur les nœuds d’événement et sont composés d’une série d’étapes. Chaque étape est une structure de trois parties : l’axe, le test de nœud et le prédicat. Pour plus d’informations sur ces éléments et sur XPath 1,0, consultez [XML Path Language (XPath)](https://www.w3.org/TR/xpath). Windows Le journal des événements impose les restrictions suivantes sur l’expression :

-   Axe : seuls les axes enfant (valeur par défaut) et attribut (et son raccourci « @ ») sont pris en charge.
-   Tests de nœud : seuls les noms de nœuds et les tests NCName sont pris en charge. Le \* caractère «», qui sélectionne n’importe quel caractère, est pris en charge.
-   Prédicats : toute expression XPath valide est acceptable si les chemins d’accès d’emplacement sont conformes aux restrictions suivantes :
    -   Les opérateurs standard **ou**, **et**, =, ! =, <=, <, >=, > et les parenthèses sont pris en charge.
    -   La génération d’une valeur de chaîne pour un nom de nœud n’est pas prise en charge.
    -   L’évaluation dans l’ordre inverse n’est pas prise en charge.
    -   Les jeux de nœuds ne sont pas pris en charge.
    -   L’étendue de l’espace de noms n’est pas prise en charge.
    -   Les nœuds d’espace de noms, de traitement et de commentaire ne sont pas pris en charge.
    -   La taille du contexte n’est pas prise en charge.
    -   Les liaisons de variables ne sont pas prises en charge.
    -   La fonction position et sa référence de tableau abrégée sont prises en charge (sur les nœuds terminaux uniquement).
    -   La fonction de bande est prise en charge. La fonction effectue une opération de bits AND pour deux arguments de nombre entier. Si le résultat de l’opération de bits AND est différent de zéro, la fonction prend la valeur true ; dans le cas contraire, la fonction prend la valeur false.
    -   La fonction timediff est prise en charge. La fonction calcule la différence entre le deuxième argument et le premier argument. L’un des arguments doit être un nombre littéral. Les arguments doivent utiliser la représentation FILETIME. Le résultat est le nombre de millisecondes entre les deux heures. Le résultat est positif si le deuxième argument représente une heure ultérieure ; dans le cas contraire, il est négatif. Lorsque le deuxième argument n’est pas fourni, l’heure système actuelle est utilisée.

 

 
