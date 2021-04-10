---
description: Traitement de l’entrée et de la sortie MFT du codec
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Traitement de l’entrée et de la sortie MFT du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201855"
---
# <a name="processing-codec-mft-input-and-output"></a>Traitement de l’entrée et de la sortie MFT du codec

Lorsque vous avez configuré le type d’entrée et le type de sortie pour une table MFT, vous pouvez commencer à traiter les exemples de données. Vous transmettez des exemples à la MFT en vue de leur traitement à l’aide de la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , puis vous récupérez l’exemple traité en appelant [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés. Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo. Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



