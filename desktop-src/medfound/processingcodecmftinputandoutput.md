---
description: Traitement de l’entrée et de la sortie MFT du codec
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Traitement de l’entrée et de la sortie MFT du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101838"
---
# <a name="processing-codec-mft-input-and-output"></a>Traitement de l’entrée et de la sortie MFT du codec

Lorsque vous avez configuré le type d’entrée et le type de sortie pour une table MFT, vous pouvez commencer à traiter les exemples de données. Vous transmettez des exemples à la MFT en vue de leur traitement à l’aide de la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , puis vous récupérez l’exemple traité en appelant [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés. Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo. Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



