---
title: Le volume scalaire
description: Le volume scalaire
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Interface MIDI (Musical Instrument Digital Interface), volume Scalar
- MIDI (Musical Instrument Digital Interface), volume Scalar
- Mappeur MIDI, volume scalaire
- scalaire de volume
- Mappeur MIDI, ajustement des niveaux de sortie
- ajustement des niveaux de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029869"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="b4a25-109">Le volume scalaire</span><span class="sxs-lookup"><span data-stu-id="b4a25-109">The Volume Scalar</span></span>

<span data-ttu-id="b4a25-110">L’objectif du volume scalaire est de permettre des ajustements entre les niveaux de sortie relatifs de différents correctifs sur un synthétiseur.</span><span class="sxs-lookup"><span data-stu-id="b4a25-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="b4a25-111">Par exemple, si le correctif Bass sur un synthétiseur est trop bruyant par rapport à son carreau piano, vous pouvez modifier la carte d’installation pour mettre à l’échelle le volume de basses ou le volume de piano.</span><span class="sxs-lookup"><span data-stu-id="b4a25-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="b4a25-112">Le volume Scalar spécifie une valeur de pourcentage pour la modification de tous les messages de contrôleur de volume principal MIDI qui suivent un message de modification de programme associé.</span><span class="sxs-lookup"><span data-stu-id="b4a25-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="b4a25-113">Par exemple, si la valeur de volume Scalar est 50%, le Mappeur MIDI modifie les messages MIDI principal-Volume Controller comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="b4a25-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![image du mappeur midi](images/mmap-a04.gif)

 

 




