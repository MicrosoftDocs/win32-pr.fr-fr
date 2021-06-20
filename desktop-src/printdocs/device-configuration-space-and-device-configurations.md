---
title: Espace de configuration de l’appareil
description: L’espace de configuration d’un appareil est l’ensemble de toutes les valeurs possibles qui peuvent être affectées à tous les attributs de l’appareil.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4871da3695e81168d43504456c357b0cf566b7f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409482"
---
# <a name="device-configuration-space-and-device-configurations"></a>Configuration de l’appareil et de l’espace de configuration des appareils

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’espace de *configuration* d’un appareil est l’ensemble de toutes les valeurs possibles qui peuvent être affectées à tous les attributs de l’appareil. Les deux raisons les plus importantes pour décrire l’espace de configuration de l’appareil dans le PrintCapabilities sont les suivantes.

1.  Les informations contribuent de manière significative à une meilleure compréhension des capacités de l’appareil. Ces informations permettent à un client du PrintCapabilities de générer plus facilement des éléments d’interface utilisateur, ce qui permet à l’utilisateur final de sélectionner plus facilement une configuration particulière pour traiter un travail. En fournissant plus de détails sur les fonctionnalités de l’appareil à l’application et finalement à l’utilisateur final, l’intention d’impression de l’utilisateur peut être plus efficace.

2.  Certaines propriétés d’appareil présentées dans PrintCapabilities peuvent dépendre de la configuration particulière sélectionnée par le client.

Certaines informations ne doivent pas être incorporées dans le PrintCapabilities. Cela comprend des informations qui n’affectent pas la manière dont un travail est créé, n’impose pas de contraintes sur la façon dont un travail est créé, ni affecte les propriétés de l’appareil. Par exemple, un appareil peut être en mesure de signaler des informations d’État, telles que l’ensemble des tâches en attente de traitement. Ces informations n’ont aucun effet sur les informations nécessaires au formatage du travail, ni sur les fonctionnalités disponibles dans l’appareil. Pour cette raison, ce type d’informations n’a pas besoin d’être présent dans le PrintCapabilities.

## <a name="device-constraints"></a>Contraintes de l’appareil

De nombreux appareils ne prennent pas en charge toutes les configurations possibles dans l’espace de configuration en raison d’une contrainte sur l’appareil. Par exemple, un appareil peut être obligé d’effectuer une impression recto-verso sur un support transparent. Une contrainte peut représenter une limitation physique : certains types de média sont tout simplement trop rigides pour parcourir certains chemins d’accès papier du périphérique, et ne peuvent donc pas être placés dans des emplacements d’entrée ou être acheminés vers certains bacs de sortie. Actuellement, il est de la responsabilité du fournisseur PrintCapabilities ou PrintTicket de valider la configuration représentée par l’entrée PrintTicket, afin de vérifier qu’elle ne représente pas une configuration non valide. Si la configuration n’est pas valide, le fournisseur PrintCapabilities ou PrintTicket doit modifier la configuration de façon à ce qu’elle devienne valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



