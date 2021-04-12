---
description: Traitement de l’entrée et de la sortie du codec DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Traitement de l’entrée et de la sortie du codec DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318741"
---
# <a name="processing-codec-dmo-input-and-output"></a>Traitement de l’entrée et de la sortie du codec DMO

Lorsque vous avez configuré le type d’entrée et le type de sortie pour un DMO, vous pouvez commencer à traiter les exemples de données. Vous transmettez des exemples à DMO pour traitement à l’aide de la méthode **IMediaObject ::P rocessinput** , puis vous récupérez l’exemple traité en appelant **IMediaObject ::P rocessoutput**. Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés. Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo. Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



