---
title: exemples de supports (kit de développement logiciel (SDK) Windows media Format 11)
description: en savoir plus sur les exemples de supports dans le kit de développement logiciel (SDK) Windows media Format 11. Un exemple de média est un objet qui contient une liste triée de zéro ou plusieurs mémoires tampons.
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, exemples de supports
- Windows Media Format SDK, exemples
- ASF (Advanced Systems Format), exemples de supports
- ASF (Advanced Systems Format), exemples de supports
- ASF (Advanced Systems Format), exemples
- ASF (format avancé des systèmes), exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741641bfa326357114f5a02e81a32ac47691661f331355d91a2c3e187ad4233b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654583"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>exemples de supports (kit de développement logiciel (SDK) Windows media Format 11)

Un échantillon de support, ou échantillon, est un bloc de données multimédias numériques. un exemple est l’unité de base manipulée par les objets de lecture et d’écriture du kit de développement logiciel (SDK) de Format multimédia Windows. Le contenu d’un exemple individuel est dicté par le type de média associé à l’exemple. Pour les vidéos, chaque échantillon représente un frame unique. Pour le son, la quantité de données dans un échantillon individuel est définie dans le profil utilisé pour créer le fichier ASF.

Les exemples peuvent contenir des données non compressées, ou elles peuvent contenir des données compressées, auquel cas ils sont appelés *exemples de flux*. Lors de la création d’un fichier ASF, vous transmettez des exemples au writer. L’enregistreur coordonne la compression des exemples avec le codec approprié et organise les données compressées dans la section de données du fichier ASF. Lors de la lecture, le lecteur lit les données compressées, les décompresse et fournit les données non compressées reconstruites comme exemples de sortie.

tous les exemples utilisés par le kit de développement logiciel (sdk) Windows Media Format sont encapsulés dans un objet buffer dont la mémoire est allouée automatiquement par les composants runtime du SDK. Vous pouvez également allouer vos propres tampons, si nécessaire, à l’aide des fonctionnalités avancées du writer et du lecteur.

**Remarque** Le terme exemple est utilisé dans ce kit de développement logiciel (SDK) pour faire référence à un exemple de support, et non à un exemple audio. Dans l’encodage audio, un exemple fait référence à une seule valeur audio encodée. En règle générale, la qualité de l’audio encodé est spécifiée par un nombre d’échantillons par seconde. Par exemple, le son de qualité CD est enregistré à 44 100 échantillons par seconde. Cette valeur est généralement abrégée avec la notation Hz, donc 44 100 échantillons par seconde sont 44 100 Hz ou 44,1 kHz.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Concepts**](concepts.md)
</dt> <dt>

[**Interface INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




