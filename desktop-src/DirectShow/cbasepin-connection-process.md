---
description: Processus de connexion CBasePin
ms.assetid: 4b3a9023-0267-4caa-9d89-88237009df05
title: Processus de connexion CBasePin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1441b0daba58857e00da0139d3312fb277287fc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999356"
---
# <a name="cbasepin-connection-process"></a>Processus de connexion CBasePin

Cette section décrit comment la classe [**CBasePin**](cbasepin.md) implémente le processus de connexion de code confidentiel.

le gestionnaire de Graph de filtre lance toutes les connexions de code confidentiel. elle appelle la méthode [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) de la broche de sortie, en spécifiant la broche d’entrée. La broche de sortie termine la connexion en appelant la méthode [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) du code confidentiel d’entrée. La broche d’entrée peut accepter ou refuser la connexion.

le gestionnaire de Graph de filtre peut également spécifier un type de média pour la connexion. Si c’est le cas, les broches essaient de se connecter avec ce type. Si ce n’est pas le cas, les broches doivent négocier le type. le gestionnaire de Graph de filtre peut également spécifier un type de média *partiel* , qui a la valeur GUID \_ NULL pour le type principal, le sous-type ou le type de format. Dans ce cas, les broches essaient de correspondre aux parties du type de média spécifiées ; la valeur du GUID \_ null agit comme un caractère générique.

la méthode [**CBasePin :: Connecter**](cbasepin-connect.md) commence par vérifier que le code confidentiel peut accepter une connexion. Par exemple, il vérifie que le pin n’est pas déjà connecté. Elle délègue le reste du processus de connexion à la méthode [**CBasePin :: AgreeMediaType**](cbasepin-agreemediatype.md) . Tout ce qui suit est effectué par **AgreeMediaType**.

Si le type de média est entièrement spécifié, le code PIN appelle la méthode [**CBasePin :: AttemptConnection**](cbasepin-attemptconnection.md) pour tenter la connexion. Dans le cas contraire, il tente des types de médias dans l’ordre suivant :

1.  Types préférés de la broche d’entrée.
2.  Types préférés de la broche de sortie.

Vous pouvez inverser cet ordre en affectant à l’indicateur [**CBasePin :: m \_ BTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md) la **valeur true**.

Dans chaque cas, le code PIN appelle [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) pour énumérer les types de médias. Cette méthode récupère un objet énumérateur, qui est passé à la méthode [**CBasePin :: TryMediaTypes**](cbasepin-trymediatypes.md) . La méthode **TryMediaTypes** parcourt chaque type de média et appelle [**AttemptConnection**](cbasepin-attemptconnection.md) pour chaque type.

Dans la méthode [**AttemptConnection**](cbasepin-attemptconnection.md) , la broche de sortie appelle les méthodes suivantes :

-   Il appelle [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) sur lui-même pour vérifier si la broche d’entrée est appropriée.
-   Il appelle [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) sur lui-même pour valider le type de média.
-   Elle appelle [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée. La broche d’entrée utilise cette méthode pour déterminer si elle doit accepter la connexion.
-   Il appelle [**CBasePin :: CompleteConnect**](cbasepin-completeconnect.md) sur lui-même pour terminer la connexion.

Notez les points suivants :

-   [**CheckConnect**](cbasepin-checkconnect.md) est une méthode virtuelle. Dans la classe de base, cette méthode vérifie si les directions de code confidentiel sont compatibles. Les broches de sortie doivent se connecter aux broches d’entrée, et vice versa. La classe pin dérivée se substitue généralement à cette méthode pour effectuer d’autres vérifications. Par exemple, il peut interroger l’autre code confidentiel pour une interface requise pour la connexion. Si la classe dérivée se substitue à **CheckConnect**, elle doit également appeler la méthode [**CBasePin**](cbasepin.md) .
-   [**CheckMediaType**](cbasepin-checkmediatype.md) est une méthode virtuelle pure, que la classe dérivée doit implémenter.
-   [**CompleteConnect**](cbasepin-completeconnect.md) est une méthode virtuelle qui ne fait rien dans la classe de base. Les classes dérivées peuvent substituer cette méthode pour exécuter tout travail supplémentaire nécessaire pour terminer la connexion, par exemple pour choisir un allocateur de mémoire.

Si l’une de ces étapes échoue, la broche de sortie appelle la méthode [**CBasePin :: BreakConnect**](cbasepin-breakconnect.md) pour annuler toutes les étapes effectuées par [**CheckConnect**](cbasepin-checkconnect.md).

La méthode [**ReceiveConnection**](cbasepin-receiveconnection.md) de la broche d’entrée appelle les méthodes [**CheckConnect**](cbasepin-checkconnect.md), [**CheckMediaType**](cbasepin-checkmediatype.md)et [**CompleteConnect**](cbasepin-completeconnect.md) du code confidentiel d’entrée. Si l’une de ces erreurs échoue, la tentative de connexion échoue également.

Le diagramme suivant illustre le processus de connexion dans [**CBasePin**](cbasepin.md):

![processus de connexion cbasepin](images/cbasepin-connect.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CBasePin**](cbasepin.md)
</dt> </dl>

 

 



