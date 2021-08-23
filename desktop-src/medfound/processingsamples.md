---
description: traitement du Codec DMO entrée et sortie
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: traitement du Codec DMO entrée et sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3b159ea9e8a323a8e980b9dbba227aa2a62d76316b90e09f45592044091f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035087"
---
# <a name="processing-codec-dmo-input-and-output"></a>traitement du Codec DMO entrée et sortie

lorsque vous avez configuré le type d’entrée et le type de sortie pour un DMO, vous pouvez commencer à traiter des exemples de données. vous transmettez des exemples au DMO pour le traitement à l’aide de la méthode **IMediaObject ::P rocessinput** , puis vous récupérez l’exemple traité en appelant **IMediaObject ::P rocessoutput**. Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés. Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo. Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



