---
title: Heure de présentation
description: Heure de présentation
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK, durée de présentation
- ASF (Advanced Systems Format), temps de présentation
- ASF (format de systèmes avancés), durées de présentation
- durées de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411358"
---
# <a name="presentation-time"></a>Heure de présentation

Une heure de présentation est une mesure du temps à partir du premier exemple du premier flux dans un fichier ASF. Cette mesure, ainsi que la plupart des autres mesures de temps utilisées par les objets de ce kit de développement logiciel (SDK), sont en unités de 100 nanosecondes. Les durées de présentation sont importantes car elles permettent aux différents flux d’un fichier d’être synchronisés. Vous devez fournir une durée de présentation pour chaque exemple d’entrée que vous transmettez au writer. Chaque objet de données de la section de données d’un fichier ASF est associé à une heure de présentation. Chaque exemple de sortie récupéré par le lecteur présente également une heure de présentation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Exemples de supports**](media-samples.md)
</dt> </dl>

 

 




