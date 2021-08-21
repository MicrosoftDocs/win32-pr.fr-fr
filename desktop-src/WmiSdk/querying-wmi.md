---
description: l’un des principaux outils de Windows Management Instrumentation (WMI) est la capacité à interroger le référentiel wmi pour obtenir des informations sur les classes et les instances.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Interrogation de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817537"
---
# <a name="querying-wmi"></a>Interrogation de WMI

l’un des principaux outils de Windows Management Instrumentation (WMI) est la capacité à interroger le référentiel wmi pour obtenir des informations sur les classes et les instances. Par exemple, vous pouvez demander que WMI retourne tous les objets représentant les événements d’arrêt à partir de votre système de bureau. Vous pouvez également récupérer des données de classe, d’instance ou de schéma. Le tableau suivant répertorie les différents types de requêtes que vous pouvez effectuer.



| Rubrique                                                                | Description                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Appel d’une requête synchrone](invoking-a-synchronous-query.md)     | Décrit comment conserver un lien avec WMI tout au long du processus de requête. Les requêtes synchrones sont efficaces pour les requêtes ou les requêtes de petite taille sur un système local.<br/>                                  |
| [Appel d’une requête asynchrone](invoking-an-asynchronous-query.md) | Décrit comment configurer un processus distinct pour recevoir des requêtes. Les requêtes asynchrones sont plus complexes et offrent un niveau de sécurité inférieur, mais améliorent généralement les performances du système.<br/> |



 

Outre l’interrogation de l’espace de stockage WMI, vous pouvez également utiliser le [*langage de requêtes WMI (WQL) (WQL)*](gloss-w.md) pour acheminer les événements de notification vers votre application. Pour plus d’informations, consultez [réception d’un événement WMI](receiving-a-wmi-event.md).

> [!Note]
>
> Pour interroger correctement WMI, vous devez avoir une bonne compréhension de WQL. Une requête incorrecte, trop complexe ou inappropriée peut entraîner le retour d’une erreur ou des résultats inattendus par le processeur de requêtes. Pour obtenir un guide complet sur WQL, consultez [interrogation avec WQL](querying-with-wql.md).
>
> Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL. Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de  **\_ \_ \_ violation de quota E WBEM** en tant que valeur HRESULT. La limite des mots clés WQL dépend de la complexité de la requête.
>
> Lors de l’interrogation des valeurs de propriété avec un type de données **UInt64** ou **sint64** dans un langage de script tel que VBScript, WMI retourne des valeurs de chaîne. Des résultats inattendus peuvent se produire lors de la comparaison de ces valeurs, car la comparaison de chaînes retourne différents résultats que la comparaison de nombres. Par exemple, « 10 milliards » est inférieur à « 9 » lors de la comparaison de chaînes et 9 est inférieur à 10 milliards lors de la comparaison de nombres. Pour éviter toute confusion, vous devez utiliser la méthode [CDbl](/previous-versions//ftekwwt0(v=vs.85)) dans VBScript lorsque les propriétés de type **UInt64** ou **sint64** sont récupérées à partir de WMI.

 

> [!Note]  

 

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

 

