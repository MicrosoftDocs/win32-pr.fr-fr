---
title: Flux de données arbitraires personnalisées
description: Flux de données arbitraires personnalisées
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media Format SDK, flux de données arbitraires personnalisés
- ASF (Advanced Systems Format), flux de données arbitraires personnalisés
- ASF (format de systèmes avancés), flux de données arbitraires personnalisés
- Windows Media Format SDK, Streams
- ASF (Advanced Systems Format), flux
- ASF (format de systèmes avancés), flux
- flux de données arbitraires personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde40c7283620aba9c0bbdd0a1b376538ce7e4f22ac12e9fcdfe78d75195a516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027937"
---
# <a name="custom-arbitrary-data-streams"></a>Flux de données arbitraires personnalisées

Vous pouvez créer un flux dans un fichier ASF pour contenir n’importe quel type de données. Si aucun des types de flux pris en charge ne répond à vos besoins, vous devez utiliser un flux de données arbitraire. L’objet writer gère un flux de données arbitraire de la même manière qu’un flux non compressé. les exemples sont paquets et combinés avec les exemples d’autres flux dans la section de données du fichier. Bien entendu, seule une application de lecture qui a été spécifiquement programmée pour gérer votre type arbitraire sera en mesure de gérer les données une fois qu’elles sont fournies par l’objet de lecture.

Une utilisation courante des flux de données arbitraires concerne les données multimédias encodées à l’aide d’un codec tiers. Étant donné que les objets de ce kit de développement logiciel (SDK) n’interagissent pas directement avec les codecs tiers, votre application d’écriture doit traiter les exemples avec la partie encodage du codec et transmettre les exemples compressés au writer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraire**](arbitrary-streams.md)
</dt> <dt>

[**Configuration de Flux arbitraires personnalisés**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




