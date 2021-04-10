---
title: Modification des interfaces d’une manière à compatibilité descendante
description: Les méthodes expliquées dans la théorie de la gestion des versions pour RPC et COM peuvent être inacceptables pour de nombreuses raisons.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314daecc6b55aaf4a348411010eb578149f86921
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729804"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Modification des interfaces d’une manière à compatibilité descendante

Les méthodes expliquées dans [la théorie de la gestion des versions pour RPC et com](the-versioning-theory-for-rpc-and-com.md) peuvent être inacceptables pour de nombreuses raisons. La modification d’une version d’interface selon les règles exige essentiellement que les nouveaux clients ne communiquent pas avec les anciens serveurs. Cela est souvent impossible avec les logiciels commerciaux déployés dans le domaine. Parfois, Windows a introduit des modifications d’interface absentes des GUID ou versions modifiés. Cela était dû au fait que de nouveaux clients ont besoin de communiquer avec des serveurs hérités et que la solution qu’un nouveau client prennait en charge à la fois les anciennes et nouvelles interfaces était jugée indésirable.

## <a name="best-practice"></a>Bonne pratique

Il s’agit des méthodes raisonnables de contournement du problème d’incompatibilité de câble lorsque le GUID et la version de l’interface ne peuvent pas être modifiés.

1.  Faire en sorte que l’application soit consciente des capacités de l’autre côté.

    Le client et le serveur ont un protocole qui permet à chacun (ou au moins au nouveau client) d’établir l’identité du partenaire. En général, il suffit que le nouveau client prenne en charge les fonctionnalités prises en charge par les anciens et nouveaux serveurs. Cela peut être facilement fait quand une application s’exécute sur un contexte de connexion et être prise en charge par le biais d’un *XxxGetInfo* type d’appel de fonction exécuté par le client avant d’effectuer des opérations RPC. Quand une application gère les fonctionnalités sur la base d’une version par serveur, un appel avec une incompatibilité avec l’ancien serveur/client ne peut jamais se produire, puisque l’application contrôle les appels émis vers le serveur. La ligne inférieure est que l’application est proactive pour empêcher une incompatibilité. Cela peut être effectué conjointement avec la deuxième pratique.

2.  Introduisez une nouvelle API distante.

    Une nouvelle méthode distante n’entre pas en conflit avec les méthodes existantes si elle est ajoutée à la fin de l’interface. Les anciens clients peuvent appeler de nouveaux serveurs comme ils le font toujours. Le nouveau client peut appeler la nouvelle méthode sans connaître l’identité du serveur, à condition qu’il surveille les erreurs provenant du serveur appelé. Le temps d’exécution RPC vérifie toujours le numéro de la méthode pour chaque interface avant une distribution pour s’assurer que la méthode se trouve dans une table v appropriée. Pour une méthode inconnue pour un serveur, la durée d’exécution RPC déclenche l’exception RPC \_ S \_ PROCNUM \_ hors \_ \_ limites. Cette exception est déclenchée uniquement dans cette situation particulière. Par conséquent, un nouveau client peut surveiller l’exception en tant que signe que l’appel a été passé à un ancien serveur et peut modifier son comportement de manière appropriée.

3.  Introduisez de nouveaux paramètres ou de nouveaux types de données uniquement dans les nouvelles méthodes.

    L’une des raisons d’introduire une nouvelle méthode consiste à éviter l’incompatibilité des données. En principe, si un nouveau type de données est introduit ou simplement modifié, il doit être utilisé uniquement dans une nouvelle méthode (ou les méthodes). Consultez des [exemples de modifications incompatibles](examples-of-incompatible-changes.md) pour obtenir des exemples de modifications de types de données incompatibles. La seule exception notable à cette règle est décrite dans l’élément 4.

4.  Mapper de nouveaux paramètres ou de nouveaux types de données via un wrapper.

    Cette solution s’applique lorsqu’un nouveau paramètre ou type de données doit être exposé à un utilisateur, mais n’a en fait pas à être mis à distance séparément ou peut être mappé aux anciens types de données ou paramètres. Par exemple, de nombreuses API système contournent et exécutent un appel distant. Ils peuvent, ou non, faire un type de mappage des types de données connus de l’utilisateur aux types de données réellement utilisés dans l’appel RPC sous-jacent. Il est donc toujours utile d’examiner si la modification de l’interface utilisateur doit se propager en tant que modification d’une interface distante.

    Une situation similaire peut se produire lorsque l’utilisateur appelle directement une API distante, mais qu’un wrapper peut être introduit pour effectuer un nouveau mappage de type ou d’autres actions supplémentaires devenues nécessaires. Le langage IDL (Interface Definition Language) offre plusieurs moyens de faciliter ce remappage, à savoir \[ [**appeler \_ en**](/windows/desktop/Midl/call-as)tant que \] , \[ [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) \] et \[ [**\_ marshaler par câble**](/windows/desktop/Midl/wire-marshal) \] . L' \[ **appel \_ en tant qu'** \] attribut introduit un wrapper de fonction sur le client et le serveur. Les deux sont placés entre le code utilisateur et le marshaleur. Les autres attributs concernent le mappage de type direct. Pour les problèmes d’extension, \[ **appelez \_ en tant que** \] est le plus fréquemment utilisé et est plus facile à comprendre et à manipuler sans pièges.

5.  Modifiez les types de données par le biais d’une Union par défaut.

    La modification d’un attribut ou d’un type de données provoque généralement l’incompatibilité des câbles. Consultez des [exemples de modifications incompatibles](examples-of-incompatible-changes.md) pour obtenir des exemples. Toutefois, dans le cas d’une Union sans clause par défaut, l’incompatibilité peut être gérée d’une manière similaire à la casse d’une procédure hors limites, comme décrit précédemment. Ce schéma est facilement applicable aux types *XxxINFO* populaires qui utilisent des unions.

    Par exemple, un appel similaire à celui-ci

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    peut retourner des informations au niveau 1, 2 ou 3, *XxxINFO* étant une Union avec trois branches : 1, 2 et 3.

6.  Utilisez l' \[ attribut [**Range**](/windows/desktop/Midl/range) \] pour spécifier Range.

    Vous pouvez spécifier l' \[ [](/windows/desktop/Midl/range) \] attribut de plage sur un type de mise à l’échelle simple sans interrompre la compatibilité descendante. Cet attribut n’affecte pas le format de câble, mais pendant le démarshaling, RPC vérifie la valeur sur Cable pour confirmer qu’il se trouve dans la plage spécifiée dans le fichier. idl. Si ce n’est pas le cas, une \_ \_ exception de liaison non valide RPC X \_ est levée. Cela s’avère particulièrement utile si le serveur connaît la taille maximale d’un tableau dimensionné.

    Par exemple :

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

Le comportement RPC lorsque le niveau indiqué est 4 et que le ARM est manquant, dépend de la définition de l’Union. Pour une Union avec la clause default définie, RPC transmet un type indiqué dans la clause default pour tout ce qui est différent des étiquettes ARM connues (dans ce cas, toute autre valeur que 1, 2 ou 3). Pour une Union sans valeur par défaut, le unmarshaleur lève une exception, car par définition il n’y a pas de valeur par défaut vers laquelle revenir. L’exception est la \_ \_ balise RPC S non valide \_ .

Là encore, un nouveau client peut ajuster son comportement lors de la découverte qu’il a appelé un ancien serveur.

Les pratiques recommandées sont les suivantes : si un type de données accessible à distance doit être conçu et peut être étendu à l’avenir, utilisez une Union non définie par défaut dans le fichier IDL. Pour un choix donné, une Union encapsulée est légèrement plus propre.

En raison des excentriques de la représentation interne du protocole NDR64 Wire, la recommandation pour l’ajout des bras fournis plus haut dans cette section doit être qualifiée comme suit : le nouveau bras ajouté ne peut pas modifier l’alignement de l’Union, et en particulier, l’alignement le plus grand des bras ne doit pas changer. Ce n’est généralement pas un problème, car un pointeur dans ARM force l’alignement sur 8. Une conception où chaque ARM est un pointeur vers un type ARM est un bon moyen de satisfaire l’exigence.

 

 