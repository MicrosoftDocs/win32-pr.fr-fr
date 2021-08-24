---
description: Flux facultative
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Flux facultative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d7c30f783a8c13b00020c2dac62cd11e2a79d6f2ea66af01f715c3cb389853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830969"
---
# <a name="optional-streams"></a>Flux facultative

une DMO peut désigner certains de ses flux de sortie comme facultatifs. Un flux facultatif produit des données que l’application peut ignorer, soit complètement, soit sur des échantillons occasionnels. Par exemple, un flux facultatif peut contenir des informations supplémentaires sur un flux principal.

Pour déterminer si un flux est facultatif, appelez la méthode [**IMediaObject :: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) et vérifiez le paramètre *pdwFlags* . DMO les flux facultatifs retournent l' \_ \_ indicateur STREAMF de sortie \_ STREAMF ou DMO l' \_ \_ indicateur facultatif de sortie \_ . Ces indicateurs ont presque la même signification ; une différence mineure entre les deux sera expliquée sous peu.

si un flux est facultatif, le client peut demander à l’DMO d’ignorer les données de ce flux lors du traitement de la sortie. Pour ce faire, appelez la méthode [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) et affectez la **valeur null** à la mémoire tampon de sortie pour chaque flux que vous souhaitez ignorer. (la mémoire tampon de sortie est spécifiée dans le membre **pBuffer** de la [**DMO \_ \_ \_ mémoire tampon de données de sortie**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer).) définissez également le DMO \_ sortie du processus \_ \_ ignorée \_ quand \_ aucun \_ indicateur de mémoire tampon n’est défini dans le paramètre *dwFlags* .

pour chaque flux où le pointeur *pBuffer* a la **valeur NULL**, le DMO tentera d’ignorer les données. si le flux est facultatif, les DMO sont assurées d’ignorer les données. si le flux n’est pas facultatif, le DMO ignore les données lorsque cela est possible, mais n’est pas sûr de le faire. s’il ne peut pas ignorer les données, il définit le DMO \_ \_ \_ \_ indicateur incomplete des données de sortie BUFFERF. si vous définissez un pointeur *pBuffer* sur la **valeur NULL** , mais que vous ne définissez pas l’DMO \_ sortie du processus \_ \_ ignorée \_ quand \_ aucun indicateur de \_ mémoire tampon n’est défini, le DMO n’ignore pas les données. dans ce cas, le DMO met en mémoire tampon la sortie en interne, ou fait simplement échouer l’appel **ProcessOutput** .

la seule différence fonctionnelle entre le DMO de \_ sortie \_ STREAMF \_ indicateur facultatif et DMO \_ l' \_ indicateur STREAMF de sortie \_ peut être le suivant :

-   DMO l' \_ \_ indicateur facultatif STREAMF OUTPUT \_ indique que le client n’a pas besoin de définir un type de média sur ce flux. Toutefois, si le client commence à traiter des données sans définir le type de média pour ce flux, il doit ignorer les données de ce flux pour toute la durée de la diffusion en continu. Si vous souhaitez ignorer les échantillons de manière sélective, vous devez définir le type de média.
-   le DMO \_ \_ \_ indicateur pouvant être ignoré STREAMF indique que, bien que le flux soit facultatif, il requiert toujours un type de média.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



