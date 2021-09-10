---
title: Marshaling d’interface
description: Marshaling d’interface
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363287"
---
# <a name="interface-marshaling"></a>Marshaling d’interface

À moins que vous ne sachiez au-delà que votre interface ne sera jamais utilisée dans les limites de cloisonnement, de thread ou de processus, vous devez décider comment assurer la prise en charge du marshaling pour vos interfaces. Il existe trois façons de fournir une prise en charge du marshaling :

-   Écrivez votre propre code proxy/stub qui appelle le canal COM, qui à son tour appelle les bibliothèques Runtime RPC. En théorie, il est possible de le faire, mais dans la pratique, il est presque impossible de le faire sans beaucoup d’efforts.
-   Décrivez vos interfaces dans un fichier IDL (Interface Definition Language) et utilisez le compilateur MIDL pour générer une DLL proxy/stub. Cette méthode fournit les meilleures performances et la plus grande flexibilité en termes de types de données acceptables. À l’aide de stubs proxy générés par MIDL, vous pouvez contrôler non seulement la gestion de la mémoire, mais également le marshaling et le démarshaling de types de données complexes sur différentes plateformes.
-   Utilisez MIDL pour générer une bibliothèque de types que le système utilise pour assurer la prise en charge du marshaling au moment de l’exécution. Il s’agit du moyen le plus simple d’implémenter la prise en charge du marshaling. Il vous suffit de générer une bibliothèque de types et de l’inscrire. Vos interfaces doivent être compatibles avec Automation ( [**oleautomation**](/windows/desktop/Midl/oleautomation) ou [**Dual**](/windows/desktop/Midl/dual)), ce qui impose des restrictions sur les types de données que vous pouvez utiliser comme paramètres de méthode. toutefois, dans la plupart des cas, l’avantage d’avoir vos interfaces accessibles aux programmes écrits dans d’autres langages, tels que Microsoft Visual Basic et Java, compense les limitations relatives aux types de données.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Communication entre les objets](inter-object-communication.md)
</dt> </dl>

 

 