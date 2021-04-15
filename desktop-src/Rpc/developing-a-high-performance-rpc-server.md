---
title: Développement d’un serveur RPC à hautes performances
description: Les informations contenues dans cette section s’appliquent aux séquences de protocoles distants ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np et à Windows 2000 et Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Appel de procédure distante RPC, meilleures pratiques, développement d’un serveur hautes performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463582"
---
# <a name="developing-a-high-performance-rpc-server"></a>Développement d’un serveur RPC à hautes performances

Les informations contenues dans cette section s’appliquent aux séquences de protocoles distants : [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)et Windows 2000 et Windows XP.

Cette section traite trois aspects principaux des performances du serveur RPC :

-   [Latence et débit du réseau](network-latency-and-throughput.md)
-   [Extensibilité](scalability.md)
-   [Conseils sur les performances des appels RPC divers](miscellaneous-rpc-performance-tips.md)

La longueur du chemin d’accès du code est un autre facteur de performance principal pour RPC. La longueur du chemin de code est généralement bien comprise, et dans la mesure où la documentation et les outils sont largement disponibles sur ce sujet, cet article ne traite pas de cette rubrique.

Une règle de performance générale importante et établie à retenir lors de l’examen des performances RPC est la suivante : Rechercher le goulot d’étranglement dans le système et travailler pour le résoudre. Le goulet d’étranglement de la passerelle peut ne pas être la programmation RPC et, si tel est le cas, le réglage des performances dans RPC n’entraîne pas de performances améliorées tant que ce goulot d’étranglement n’est pas traité. Par exemple, il n’est pas nécessaire d’utiliser le réseau par le biais d’une contention de ressources.

Si votre système est déployé dans différents environnements, il est judicieux de s’assurer que tous les aspects sont bien réglés, dans la mesure où différents environnements peuvent produire des goulots d’étranglement de performances variés.

 

 