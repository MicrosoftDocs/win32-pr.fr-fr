---
title: Scénario 2 exemple d’analyseur à l’aide du suivi ETW
description: 'Pour générer un rapport de suivi ETW pour le composant API du serveur HTTP, exécutez les étapes comme indiqué dans le \ 0034 ; Génération d’un rapport de suivi ETW \ 0034 ; section du scénario 1 : exemple de délai d’expiration HTTP utilisant le suivi ETW et les commandes netsh, mais reproduire l’erreur propre à ce scénario.'
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c566973b660e4e665226fbf9b4a266b086b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031252"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Scénario 2 : exemple d’analyseur utilisant le suivi ETW

Pour générer un rapport de suivi ETW pour le composant API du serveur HTTP, exécutez les étapes décrites dans la section « génération d’un rapport de suivi ETW » de [scénario 1 : exemple de délai d’expiration http à l’aide du suivi ETW et des commandes netsh](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md), mais reproduisez l’erreur spécifique à ce scénario. Dans cet exemple, accédez à l’application Web à partir d’un ordinateur client, ce qui provoque l’affichage du message « 400 requête incorrecte » sur le client. Ces étapes sont exécutées sur le serveur, car il héberge l’application Web.

## <a name="viewing-the-trace-and-diagnosing"></a>Affichage du suivi et du diagnostic

Le fichier CSV résultant pour les traces peut être affiché dans Excel ou tout outil qui prend en charge le format CSV. Le tableau 2 ci-dessous présente des extraits d’un exemple de fichier de trace (httptrace.csv). Dans le rapport de suivi, la colonne « Level » affiche une entrée avec la valeur « 2 », qui représente une erreur. Comme indiqué ci-dessus, le composant de l’API du serveur HTTP suit les niveaux ETW définis dans l’article [LevelType type complexe de type complexe](../wes/eventmanifestschema-leveltype-complextype.md).

Les niveaux ETW sont les suivants : 1 critique ; 2 erreur ; 3 AVERTISSEMENT ; 4 informations ; 5 commentaires.

Avec cette erreur, le type d’événement (colonne de type) indique « ParseRequestFailed ». Dans les colonnes suivantes de l’événement ParseRequestFailed, nous voyons une entrée « InvalidHost ». Cette entrée signifie que l’hôte identifié dans la requête HTTP est incorrect, conformément au protocole HTTP. Notez que la colonne avec l’entrée « InvalidHost » n’est pas incluse dans le tableau pour des raisons de concision et pour éviter l’extrait de colonnes non contiguës.

Pour résoudre ce problème d’analyse, le client Web doit être corrigé pour être conforme à la norme RFC HTTP. 

| Nom d'événement                    | Type               | ID de l’événement | Version | Channel | Level |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | En-tête             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

Tableau 2 : extraits d’un exemple de rapport de suivi d’un problème d’analyse

 

 