---
title: Détails du marshaling
description: Si vous utilisez le marshaling standard, COM gère tous les détails décrits ici pour vous.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0fd46ee29c712c6f2b5b286df76a30f1047e6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106523737"
---
# <a name="marshaling-details"></a>Détails du marshaling

Si vous utilisez le marshaling standard, COM gère tous les détails décrits ici pour vous. Toutefois, il existe des programmeurs qui ont besoin de ces informations et pour ceux qui s’intéressent aux informations sous-jacentes. Le marshaling est le processus d’empaquetage et de désassemblage des paramètres pour qu’un appel de procédure distante puisse avoir lieu.

Les différents types de paramètres sont marshalés de différentes façons. Par exemple, le marshaling d’un paramètre entier implique simplement de copier la valeur dans la mémoire tampon des messages. (Même si, même dans ce cas simple, il y a des problèmes tels que l’ordonnancement des octets pour traiter les appels entre ordinateurs.) Le marshaling d’un tableau est toutefois un processus plus complexe. Les membres du tableau sont copiés dans un ordre spécifique afin que l’autre partie puisse reconstruire le tableau exactement. Lorsqu’un pointeur est marshalé, les données vers lesquelles le pointeur pointe sont copiées et les règles et conventions suivantes pour traiter les pointeurs imbriqués dans les structures. Des fonctions uniques existent pour gérer le marshaling de chaque type de paramètre.

Avec le marshaling standard, les proxies et les stubs sont des ressources à l’échelle du système pour l’interface et ils interagissent avec le canal via un protocole standard. Le marshaling standard peut être utilisé à la fois par les interfaces définies par COM standard et par les interfaces personnalisées, comme suit :

-   Dans le cas de la plupart des interfaces COM, les proxies et les stubs pour le marshaling standard sont des objets de composant in-process qui sont chargés à partir d’une DLL du système fournie par COM dans Ole32.dll.
-   Dans le cas d’interfaces personnalisées, les proxies et les stubs pour le marshaling standard sont générés par le concepteur d’interface, en général avec MIDL. Ces proxys et stubs étant configurés de manière statique dans le registre, tout client potentiel peut utiliser l’interface personnalisée à travers les limites du processus. Ces proxies et stubs sont chargés à partir d’une DLL localisée via le registre système, à l’aide de l’ID d’interface (IID) de l’interface personnalisée qu’ils marshalent.
-   Une alternative à l’utilisation de MIDL pour générer des proxies et des stubs pour les interfaces personnalisées, une bibliothèque de types peut être générée à la place et le système fourni, type-libraryâ, le moteur de marshaling piloté marshale l’interface.

Comme alternative au marshaling standard, une interface (standard ou personnalisée) peut utiliser le marshaling personnalisé. Avec le marshaling personnalisé, un objet implémente dynamiquement les proxies au moment de l’exécution pour chaque interface qu’il prend en charge. Pour une interface donnée, l’objet peut sélectionner un marshaling standard fourni par COM ou un marshaling personnalisé. Ce choix est effectué par l’objet interface par interface. Une fois le choix effectué pour une interface donnée, il reste en vigueur pendant la durée de vie de l’objet. Toutefois, une interface sur un objet peut utiliser le marshaling personnalisé tandis qu’une autre utilise le marshaling standard.

Le marshaling personnalisé est fondamentalement unique pour l’objet qui l’implémente. Elle utilise des proxys implémentés par l’objet et fournis au système sur demande au moment de l’exécution. Les objets qui implémentent le marshaling personnalisé doivent implémenter l’interface [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , contrairement aux objets qui prennent en charge le marshaling standard.

Si vous décidez d’écrire une interface personnalisée, vous devez fournir une prise en charge du marshaling pour celle-ci. En règle générale, vous allez fournir une DLL de marshaling standard pour l’interface que vous concevez. Vous pouvez créer le code proxy/stub et la DLL proxy/stub, ou vous pouvez créer une bibliothèque de types qui sera utilisée par COM pour effectuer un marshaling piloté par les données (à l’aide des données de la bibliothèque de types).

Pour qu’un client effectue un appel à une méthode d’interface dans un objet dans un autre processus, implique la coopération de plusieurs composants. Le proxy standard est un élément de code spécifique à l’interface qui réside dans l’espace de processus du client et prépare les paramètres d’interface pour la transmission. Les packages informatiques, ou marshalés, peuvent être recréés et compris dans le processus de réception. Le stub standard, également un morceau de code spécifique à l’interface, réside dans l’espace de processus du serveur et inverse le travail du proxy. Le stub décompresse, ou démarshale, les paramètres envoyés et les transfère à l’application objet. Il empaquette également les informations de réponse à renvoyer au client.

> [!Note]  
> Les lecteurs qui sont plus familiarisés avec RPC que COM peuvent être utilisés pour voir les termes stub client et stub serveur. Ces termes sont analogues au proxy et au stub.

 

## <a name="components-of-interprocess-communications"></a>Composants des communications interprocessus

Le diagramme suivant illustre le déroulement de la communication entre les composants impliqués. Du côté client de la limite de processus, l’appel de méthode du client passe par le proxy, puis sur le canal, qui fait partie de la bibliothèque COM. Le canal envoie la mémoire tampon contenant les paramètres marshalés à la bibliothèque Runtime RPC, qui la transmet à travers la limite du processus. Le temps d’exécution RPC et les bibliothèques COM existent des deux côtés du processus. La distinction entre le canal et le temps d’exécution RPC est une caractéristique de cette implémentation et ne fait pas partie du modèle de programmation ou du modèle conceptuel pour les objets client/serveur COM. Les serveurs COM voient uniquement le proxy ou le stub et, indirectement, le canal. Les implémentations futures peuvent utiliser des couches différentes sous le canal ou aucune couche.

![Diagramme qui montre le Client.exe et Server.exe flux de chaque côté de la limite de processus.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Communication entre les objets](inter-object-communication.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Talon](stub.md)
</dt> </dl>

 

 