---
description: L’illustration suivante montre comment deux applications peuvent partager un assembly à l’aide de la méthode traditionnelle de partage d’assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Partage d’assembly côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcfbb40040b51fc2e17d3707d4a76c7ea5ddadf1806e41b7a7fbd81860ae15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141810"
---
# <a name="side-by-side-assembly-sharing"></a>Partage d’assembly côte à côte

L’illustration suivante montre comment deux applications peuvent partager un assembly à l’aide de la méthode traditionnelle de partage d’assembly. Un problème de partage d’assembly traditionnel se produit lorsqu’une application installe une version d’un assembly (généralement une DLL) qui n’est pas à compatibilité descendante. L’application qui vient d’être installée fonctionne, mais les applications qui dépendent de la version précédente de la DLL risquent de ne plus fonctionner.

![représentation de deux applications partageant un assembly](images/sxs1.png)

L’application isolée et la solution d’assembly côte à côte permettent à différentes versions du même assembly Win32 de s’exécuter en même temps sur le même système sans conflit. En spécifiant la version d’assembly côte à côte que l’application doit utiliser, les développeurs peuvent garantir que la configuration testée sera toujours dupliquée sur l’ordinateur de l’utilisateur. Le partage côte à côte est illustré dans la figure suivante.

![implémentation du partage d’assembly côte à côte](images/sxs2.png)

Pour plus d’informations, consultez [à propos des applications isolées et des assemblys côte à côte](about-isolated-applications-and-side-by-side-assemblies.md).

 

 



