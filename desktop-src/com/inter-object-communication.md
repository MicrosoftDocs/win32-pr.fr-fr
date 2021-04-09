---
title: Communication Inter-Object
description: COM est conçu pour permettre aux clients de communiquer de manière transparente avec des objets, quel que soit l’emplacement d’exécution de ces objets dans le même processus, sur le même ordinateur ou sur un autre ordinateur.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102385"
---
# <a name="inter-object-communication"></a>Communication Inter-Object

COM est conçu pour permettre aux clients de communiquer de manière transparente avec des objets, quel que soit l’emplacement où ces objets sont runningâs, dans le même processus, sur le même ordinateur ou sur un autre ordinateur. Cela fournit un modèle de programmation unique pour tous les types d’objets, et pour les clients d’objets et les serveurs d’objets.

Du point de vue du client, tous les objets sont accessibles par le biais de pointeurs d’interface. Un pointeur doit être in-process. En fait, tout appel à une fonction d’interface atteint toujours un morceau de code in-process. Si l’objet est in-process, l’appel l’atteint directement, sans code d’infrastructure système intermédiaire. Si l’objet est hors processus, l’appel commence par atteindre ce qui est appelé un objet « proxy » fourni par COM ou par l’objet (si le responsable de l’implémentation le souhaite). Les packages de proxy appellent des paramètres (y compris tous les pointeurs d’interface) et génèrent l’appel de procédure distante approprié (ou tout autre mécanisme de communication dans le cas de proxies générés personnalisés) à l’autre processus ou à l’autre ordinateur sur lequel se trouve l’implémentation de l’objet. Ce processus d’empaquetage de pointeurs pour la transmission à travers les limites de processus est appelé *marshaling*.

Du point de vue d’un serveur, tous les appels aux fonctions d’interface d’un objet sont effectués à l’aide d’un pointeur vers cette interface. Là encore, un pointeur a un contexte uniquement dans un processus unique, et l’appelant doit toujours être un morceau de code in-process. Si l’objet est in-process, l’appelant est le client lui-même. Dans le cas contraire, l’appelant est un objet « stub » fourni par COM ou par l’objet lui-même. Le stub reçoit l’appel de procédure distante (ou un autre mécanisme de communication dans le cas de proxys générés personnalisés) du « proxy » dans le processus client, démarshale les paramètres et appelle l’interface appropriée sur l’objet serveur. Des points de vue des clients et des serveurs, ils communiquent toujours directement avec un autre code in-process.

COM fournit une implémentation du marshaling, appelée *marshaling standard*. Cette implémentation fonctionne très bien pour la plupart des objets et réduit considérablement les exigences de programmation, ce qui rend le processus de marshaling effectivement transparent.

La séparation claire de l’interface par rapport à l’implémentation de la transparence des processus de COM peut toutefois se faire dans certains cas. La conception d’une interface qui se concentre sur sa fonction du point de vue du client peut parfois mener à des décisions de conception qui sont en conflit avec une implémentation efficace de cette interface sur un réseau. Dans ce type de situation, ce qui est nécessaire n’est pas une transparence de processus pure, mais la transparence de processus, sauf si vous avez besoin de vous en soucier. COM offre cette fonctionnalité en permettant à un implémenteur d’objet de prendre en charge le *marshaling personnalisé* (également appelé « marshaling de [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) »). Le marshaling standard est, en fait, une instance de marshaling personnalisé ; Il s’agit de l’implémentation par défaut utilisée lorsqu’un objet ne requiert pas de marshaling personnalisé.

Vous pouvez implémenter un marshaling personnalisé pour permettre à un objet d’effectuer des actions différentes lorsqu’il est utilisé à partir d’un réseau plutôt qu’à un accès local et qu’il est totalement transparent pour le client. Cette architecture permet de concevoir des interfaces client/objet sans tenir compte des problèmes de performances du réseau, puis de résoudre les problèmes de performances du réseau sans interrompre la conception établie.

COM ne spécifie pas la manière dont les composants sont structurés ; Il spécifie la manière dont ils interagissent. COM laisse la préoccupation quant à la structure interne d’un composant aux langages de programmation et aux environnements de développement. À l’inverse, les environnements de programmation n’ont pas de normes définies pour travailler avec des objets en dehors de l’application immédiate. Microsoft Visual C++, par exemple, fonctionne très bien pour manipuler des objets dans une application, mais ne prend pas en charge l’utilisation d’objets en dehors de l’application. En règle générale, tous les autres langages de programmation sont les mêmes à cet égard. Par conséquent, pour assurer l’interopérabilité des Readiness, COM, via des interfaces indépendantes du langage, reprend là où les langages de programmation restent inactifs.

La double indirection de la structure VTBL signifie que les pointeurs dans la table des pointeurs de fonction n’ont pas besoin de pointer directement vers l’implémentation réelle de l’objet réel. C’est le cœur de la transparence du processus.

Pour les serveurs in-process, où l’objet est chargé directement dans le processus client, les pointeurs de fonction dans la table pointent directement vers l’implémentation réelle. Dans ce cas, un appel de fonction du client à une méthode d’interface transfère directement le contrôle d’exécution à la méthode. Toutefois, cette opération ne peut pas être utilisée pour les objets locaux et distants autonomes, car les pointeurs vers la mémoire ne peuvent pas être partagés entre les processus. Néanmoins, le client doit être en mesure d’appeler les méthodes d’interface comme s’il appelait l’implémentation réelle. Ainsi, le client transfère uniformément le contrôle à une méthode dans un objet en effectuant l’appel.

Un client appelle toujours des méthodes d’interface dans un objet in-process. Si l’objet réel est local ou distant, l’appel est effectué à un objet proxy, qui effectue ensuite un appel de procédure distante vers l’objet réel.

Quelle est la méthode réellement exécutée ? La réponse est qu’à chaque appel à une interface hors processus, chaque méthode d’interface est implémentée par un objet proxy. L’objet proxy est toujours un objet in-process qui agit au nom de l’objet qui est appelé. Cet objet proxy sait que l’objet réel s’exécute sur un serveur local ou distant.

L’objet proxy conditionne les paramètres de fonction dans certains paquets de données et génère un appel RPC à l’objet local ou distant. Ce paquet est récupéré par un objet stub dans le processus du serveur sur l’ordinateur local ou distant, qui décompresse les paramètres et effectue l’appel à l’implémentation réelle de la méthode. Lorsque cette fonction retourne, le stub regroupe tous les paramètres de sortie et la valeur de retour, puis les renvoie au proxy, qui les décompresse et les retourne au client d’origine.

Ainsi, le client et le serveur communiquent toujours entre eux comme si tout était en cours de traitement. Tous les appels du client et tous les appels au serveur sont, à un moment donné, dans le processus. Toutefois, étant donné que la structure VTBL permet à un agent, comme COM, d’intercepter tous les appels de fonction et tous les retours des fonctions, cet agent peut rediriger ces appels vers un appel RPC si nécessaire. Bien que les appels in-process soient plus rapides que les appels out-of-process, les différences de processus sont totalement transparentes au client et au serveur.

Pour plus d'informations, voir les rubriques suivantes :

-   [Détails du marshaling](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Talon](stub.md)
-   [Channel](channel.md)
-   [Microsoft RPC](microsoft-rpc.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> <dt>

[Marshaling d’interface](interface-marshaling.md)
</dt> </dl>

 

 