---
description: Flux facultatifs
ms.assetid: 94477a71-c267-4602-893b-1bd1256b34ef
title: Flux facultatifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940be49196396aa2d1fa71502213b0d4fbacb5ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513281"
---
# <a name="optional-streams"></a>Flux facultatifs

Un DMO peut désigner certains de ses flux de sortie comme facultatifs. Un flux facultatif produit des données que l’application peut ignorer, soit complètement, soit sur des échantillons occasionnels. Par exemple, un flux facultatif peut contenir des informations supplémentaires sur un flux principal.

Pour déterminer si un flux est facultatif, appelez la méthode [**IMediaObject :: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) et vérifiez le paramètre *pdwFlags* . Les flux facultatifs renvoient \_ l' \_ indicateur Ignorable STREAMF de sortie DMO \_ ou \_ l' \_ indicateur facultatif STREAMF de sortie DMO \_ . Ces indicateurs ont presque la même signification ; une différence mineure entre les deux sera expliquée sous peu.

Si un flux est facultatif, le client peut demander à DMO d’ignorer les données de ce flux lors du traitement de la sortie. Pour ce faire, appelez la méthode [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) et affectez la **valeur null** à la mémoire tampon de sortie pour chaque flux que vous souhaitez ignorer. (La mémoire tampon de sortie est spécifiée dans le membre **pbuffer** de la [**\_ \_ \_ mémoire tampon de données de sortie DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer).) Définissez également la \_ sortie du processus DMO \_ \_ ignorée \_ quand \_ aucun \_ indicateur de mémoire tampon n’est défini dans le paramètre *dwFlags* .

Pour chaque flux où le pointeur *pbuffer* a la **valeur null**, DMO tentera d’ignorer les données. Si le flux est facultatif, il est garanti que les données sont rejetées par DMO. Si le flux n’est pas facultatif, DMO rejette les données lorsque cela est possible, mais n’est pas sûr de le faire. S’il ne peut pas ignorer les données, il définit \_ l' \_ \_ indicateur BUFFERF Incomplete des données de sortie DMO \_ . Si vous définissez un pointeur *pbuffer* sur la **valeur null** mais que vous ne définissez pas la \_ sortie du processus DMO \_ \_ ignorée \_ quand \_ aucun indicateur de \_ mémoire tampon n’est défini, DMO n’ignore pas les données. Dans ce cas, le DMO met en mémoire tampon la sortie en interne, ou fait simplement échouer l’appel **ProcessOutput** .

La seule différence fonctionnelle entre l' \_ indicateur facultatif de sortie DMO \_ STREAMF \_ et l' \_ indicateur de suppression STREAMF de sortie DMO \_ \_ est le suivant :

-   L' \_ \_ indicateur facultatif STREAMF de sortie DMO \_ indique que le client n’a pas besoin de définir un type de média sur ce flux. Toutefois, si le client commence à traiter des données sans définir le type de média pour ce flux, il doit ignorer les données de ce flux pour toute la durée de la diffusion en continu. Si vous souhaitez ignorer les échantillons de manière sélective, vous devez définir le type de média.
-   L' \_ indicateur de \_ suppression STREAMF de sortie DMO \_ indique que, bien que le flux soit facultatif, il requiert toujours un type de média.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



