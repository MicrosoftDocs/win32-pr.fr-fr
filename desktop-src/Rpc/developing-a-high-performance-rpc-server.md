---
title: Développement d’un serveur RPC à hautes performances
description: les informations contenues dans cette section s’appliquent aux séquences de protocoles distants ncacn \_ ip \_ tcp, ncacn \_ http, ncacn \_ np et à Windows 2000 et Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- Appel de procédure distante RPC, meilleures pratiques, développement d’un serveur hautes performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021768"
---
# <a name="developing-a-high-performance-rpc-server"></a>Développement d’un serveur RPC à hautes performances

les informations contenues dans cette section s’appliquent aux séquences de protocoles distants : [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)et à Windows 2000 et Windows XP.

Cette section traite trois aspects principaux des performances du serveur RPC :

-   [Latence et débit du réseau](network-latency-and-throughput.md)
-   [Extensibilité](scalability.md)
-   [Astuces des performances RPC diverses](miscellaneous-rpc-performance-tips.md)

La longueur du chemin d’accès du code est un autre facteur de performance principal pour RPC. La longueur du chemin de code est généralement bien comprise, et dans la mesure où la documentation et les outils sont largement disponibles sur ce sujet, cet article ne traite pas de cette rubrique.

Une règle de performance générale importante et établie à retenir lors de l’examen des performances RPC est la suivante : Rechercher le goulot d’étranglement dans le système et travailler pour le résoudre. Le goulet d’étranglement de la passerelle peut ne pas être la programmation RPC et, si tel est le cas, le réglage des performances dans RPC n’entraîne pas de performances améliorées tant que ce goulot d’étranglement n’est pas traité. Par exemple, il n’est pas nécessaire d’utiliser le réseau par le biais d’une contention de ressources.

Si votre système est déployé dans différents environnements, il est judicieux de s’assurer que tous les aspects sont bien réglés, dans la mesure où différents environnements peuvent produire des goulots d’étranglement de performances variés.

 

 