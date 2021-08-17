---
title: Chaînes de format de NDR RPC
description: Chaînes de format de NDR de l’appel de procédure distante (RPC).
ms.assetid: 9c83a039-49d3-491d-8110-29d1548730de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0a481e2c992f3fd4dda2d5552fbbabb7e9b01e6eb639a092e25ba9a26bd59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926303"
---
# <a name="rpc-ndr-format-strings"></a>Chaînes de format de NDR RPC

## <a name="ndr-engine-32-bit-interpreter"></a>Moteur de NDR : interprète 32 bits

Ce document décrit les descripteurs de chaîne de format, parfois appelés éléments MOP, pour le moteur de NDR 32 bits. Cette section décrit les modifications associées à l’évolution de l’interpréteur [**– OI**](/windows/desktop/Midl/-oi) à la couche d’interpréteur de la couche d' **interfaces** , ainsi que les ajouts liés aux canaux et à la prise en charge asynchrone.

Ce document décrit la technologie MIDL (Current Microsoft Interface Definition Language) du point de vue du moteur, ainsi que le moteur de NDR actuel.

## <a name="overview"></a>Vue d’ensemble

Le moteur de NDR est le moteur de marshaling des composants RPC (Remote Procedure Call) et DCOM. Il gère tous les problèmes liés au stub d’un appel distant. En tant que processus, le marshaling de NDR est piloté par le code C des stubs générés par MIDL, un générateur de type JIT MIDL, ou par les stubs générés par d’autres outils ou écrits manuellement. À son tour, le moteur de rapport de non-remise pilote le temps d’exécution sous-jacent (DCOM ou RPC) qui communique avec des transports spécifiques.

L’objectif initial de la conception était de fournir un outil pour un marshaling efficace des données arbitraires, en fonction des informations fournies par le compilateur MIDL. Les chaînes de format décrites dans ce document (et, en effet, toutes les informations générées par le compilateur pour la consommation du moteur de NDR) ont toujours été considérées comme une interface interne entre le compilateur et le moteur. De même, les interfaces disponibles au moteur pour gérer les problèmes d’exécution sont également principalement internes (certaines exceptions existent au niveau de l’exécution RPC et certaines interfaces DCOM utilisées par le moteur sont externes).

Deux approches typiques du marshaling ont toujours été des technologies inline et pilotées par les données (interprétées). MIDL prend en charge les commutateurs [**– OS**](/windows/desktop/Midl/-os) et [**-OI \***](/windows/desktop/Midl/-oi) dans ses stubs générés en C. En outre, MIDL peut générer les bibliothèques TLB utilisées par le package oleautomation. En conséquence, une perspective des éléments internes du moteur est qu’elle se compose de deux parties.

La première est un ensemble de routines qui gèrent le dimensionnement, le marshaling, etc., correspondant aux objets de type de données typiques comme une structure ou un tableau. Ces routines sont ajustées pour des performances optimales. par exemple, ils essaient généralement de bloquer-copier des données dans la mesure du possible. Cette partie est souvent appelée moteur de rapport de rapport principal.

La deuxième partie se compose d’un interpréteur et de ses éléments associés. L’interpréteur utilise des routines du moteur de rapport de rapport principal, comme s’il s’agissait d’une bibliothèque interne, afin d’exécuter un appel distant avec tous ses arguments marshalés et démarshalés, le cas échéant.

Le moteur de détourage de la clé principale est utilisé de la même manière que celui utilisé à partir de stubs inline ou de l’interpréteur. Toutes les routines de moteur principales dépendent de l’état passé par une structure de message stub. La structure est correctement configurée par le stub inclus ou par l’interpréteur. Au fil des années, le moteur principal avait été utilisé dans un contexte différent ; actuellement, l’interpréteur est en fait un ensemble de plusieurs boucles d’interpréteurs distinctes. Celles-ci sont liées aux interpréteurs anciens et nouveaux ([**– OI**](/windows/desktop/Midl/-oi) et **-** b), ainsi qu’aux boucles relatives à la sérialisation des données (récupération), à la prise en charge asynchrone par RPC et à la prise en charge asynchrone DCOM (RPC et DCOM ont des modèles de programmation asynchrone différents).

Au-delà de l’ajout de nouvelles fonctionnalités, un aspect important de l’évolution du moteur de NDR est un changement général de l’approche des interpréteurs. NDR version 1.1 a commencé dans le cadre d’une nouvelle approche MIDL 2,0 du marshaling, avec les stubs Inline préférés pour les considérations relatives aux performances. Avec la version la plus récente du rapport de non-remise, – la norme d' [**interfaces**](/windows/desktop/Midl/-oi) est devenue le mode le plus largement utilisé du compilateur, presque à l’exclusion des stubs Inline.

Les descripteurs de chaîne de format du moteur de rapport de non-remise RPC sont décrits plus en détail dans les rubriques suivantes :

-   [Chaînes de format](format-strings.md)
-   [Chaînes de format de procédure](procedure-format-strings.md)
-   [Descripteur d’en-tête de procédure](procedure-header-descriptor.md)
-   [Poignées](handles.md)
-   [L’en-tête](the-header.md)
-   [Descripteurs de paramètre](parameter-descriptors.md)
-   [Chaînes de format de type](type-format-strings.md)

 

 