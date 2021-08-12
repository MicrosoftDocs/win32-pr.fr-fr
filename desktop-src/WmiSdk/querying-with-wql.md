---
description: le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble de American National Standards Institute standard langage SQL (ANSI SQL) avec des modifications sémantiques mineures pour prendre en charge WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Interrogation avec WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 737ae9505a0f775c26c5049eeb2f8500c9e3222d78181e18326ff53d39dfde01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554830"
---
# <a name="querying-with-wql"></a>Interrogation avec WQL

le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble de American National Standards Institute standard langage SQL (ANSI SQL) avec des modifications sémantiques mineures pour prendre en charge WMI.

pour obtenir la liste complète des mots clés wql pris en charge, consultez [wql (SQL pour WMI)](wql-sql-for-wmi.md). l’utilisation de mots clés SQL pour les noms d’objets ou de propriétés peut empêcher l’analyse d’une requête. les mots clés de SQL suivants sont restreints : **NULL**, **TRUE** et **false**.

> [!Note]  
> Il existe des limites concernant le nombre de mots clés AND et OR qui peuvent être utilisés dans les requêtes WQL. Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT. La limite des mots clés WQL dépend de la complexité de la requête.

 

Les requêtes peuvent utiliser la clause **Where** pour l’extension et la personnalisation, bien que cela ne soit pas obligatoire. La clause **Where** est constituée d’une propriété ou d’un mot clé, d’un opérateur et d’une constante. Toutes les clauses **Where** doivent spécifier l’un des opérateurs prédéfinis qui sont inclus dans WQL. Pour plus d’informations sur la syntaxe, consultez [Where, clause](where-clause.md). Pour plus d’informations sur les opérateurs WQL valides, consultez [opérateurs WQL](wql-operators.md).

comme avec d’autres chaînes de requête SQL, vous pouvez échapper vos requêtes.

> [!Note]  
> WQL ne prend pas en charge les requêtes ou les associations entre espaces de noms. Vous ne pouvez pas interroger toutes les instances d’une classe spécifiée résidant dans tous les espaces de noms sur l’ordinateur cible.

 

WQL prend en charge les types de requêtes suivants :

-   Requêtes de données

    Les requêtes de données sont utilisées pour récupérer des instances de classe et des associations de données. Il s’agit du type de requête le plus couramment utilisé dans les applications et les scripts WMI. Pour plus d’informations sur la syntaxe des requêtes de données, consultez [demande de données d’instance de classe](requesting-class-instance-data.md). Pour plus d’informations sur les associations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).

    > [!Note]  
    > WQL ne prend pas en charge les requêtes de types de données de tableau.

     

    L’exemple de requête de données suivant demande le fichier journal des événements nommé « application » à partir de toutes les instances de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Requêtes d’événements

    Les consommateurs utilisent des requêtes d’événements pour s’inscrire afin de recevoir des notifications d’événements. Les fournisseurs d’événements utilisent des requêtes d’événement pour s’inscrire afin de prendre en charge un ou plusieurs événements. Pour plus d’informations sur les requêtes d’événements, consultez [réception de notifications d’événements](receiving-event-notifications.md).

    L’exemple suivant de requête d’événement par un consommateur d’événements temporaire demande une notification lorsqu’une nouvelle instance d’une classe dérivée de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) est créée.

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   Requêtes de schéma

    Les requêtes de schéma sont utilisées pour récupérer les définitions de classe (plutôt que les instances de classe) et les associations de schéma. Les fournisseurs de classes utilisent des requêtes de schéma pour spécifier les classes qu’ils prennent en charge lorsqu’ils s’inscrivent. Pour plus d’informations sur les requêtes de schéma, consultez [extraction de définitions de classe](retrieving-class-definitions.md).

    L’exemple de requête de schéma suivant montre la syntaxe spéciale.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Format de date et d’heure WMI](date-and-time-format.md)
</dt> </dl>

 

 
