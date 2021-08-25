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
ms.openlocfilehash: a7710e8e3ceb8079f04ac97bfcce8c91c6c74aa60452c220166e358a87939848
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804943"
---
# <a name="the-volume-scalar"></a>Le volume scalaire

L’objectif du volume scalaire est de permettre des ajustements entre les niveaux de sortie relatifs de différents correctifs sur un synthétiseur. Par exemple, si le correctif Bass sur un synthétiseur est trop bruyant par rapport à son carreau piano, vous pouvez modifier la carte d’installation pour mettre à l’échelle le volume de basses ou le volume de piano.

Le volume Scalar spécifie une valeur de pourcentage pour la modification de tous les messages de contrôleur de volume principal MIDI qui suivent un message de modification de programme associé. Par exemple, si la valeur de volume Scalar est 50%, le Mappeur MIDI modifie les messages MIDI principal-Volume Controller comme indiqué dans l’illustration suivante.

![image du mappeur midi](images/mmap-a04.gif)

 

 




