---
title: Paramètres de sortie
description: Paramètres de sortie
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows Media Format SDK, constantes globales
- ASF (Advanced Systems Format), constantes globales
- ASF (format de systèmes avancés), constantes globales
- constantes globales, liste des
- Windows Media Format SDK, constantes
- ASF (Advanced Systems Format), constantes
- ASF (Advanced Systems Format), constantes
- constantes, liste
- Windows Media Format SDK, paramètres de sortie
- ASF (Advanced Systems Format), paramètres de sortie
- ASF (format des systèmes avancés), paramètres de sortie
- paramètres de sortie
- lecteurs synchrones, paramètres de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5a02d508f76057dd72e34558a7ca8d29de4847
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101233"
---
# <a name="output-settings"></a>Paramètres de sortie

Les constantes globales suivantes sont utilisées pour identifier les paramètres de sortie pour le lecteur et l’objet lecteur synchrone.



| Constante globale                | \_type de \_ données attr WMT  | Description de *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_wszAllowInterlacedOutput g    | **\_type WMT \_ bool**  | Si la valeur est true, le lecteur fournit des frames entrelacés, s’ils sont pris en charge par la sortie.                                                                                                                                                                                                                                            |
| \_wszDedicatedDeliveryThread g  | **\_type WMT \_ bool**  | Si la valeur est true, ce résultat aura un thread dédié créé pour la remise de ses échantillons. Non pris en charge sur le lecteur synchrone.                                                                                                                                                                                            |
| \_wszDeliverOnReceive g         | **\_type WMT \_ bool**  | Si la valeur est true, les exemples de cette sortie sont remis dès qu’ils sont disponibles à partir du lecteur. Cela peut entraîner la remise dans le désordre des échantillons de cette sortie et avant les échantillons correspondants d’autres sorties.                                                                                            |
| \_wszDynamicRangeControl g      | **\_valeur DWORD de type WMT \_** | Spécifie le niveau de contrôle de plage dynamique à utiliser pour la sortie. Défini sur une valeur comprise entre 0 et 2, où 0 indique qu’il n’y a pas de contrôle de plage dynamique (valeur par défaut) et 2 le niveau maximal de contrôle de plage dynamique (la plus petite plage dynamique).                                                                                |
| \_wszEarlyDataDelivery g        | **\_valeur DWORD de type WMT \_** | Durée, en millisecondes, qui spécifie le niveau de remise des échantillons. Si la valeur est supérieure à zéro, les exemples de cette sortie sont récupérés et décodés afin que les exemples soient livrés plus tôt que les exemples pour d’autres sorties. Normalement, le lecteur fournit des exemples par ordre de durée de présentation.         |
| \_wszEnableDiscreteOutput g     | **\_type WMT \_ bool**  | Si la valeur est true, le lecteur active la sortie audio multicanal haute définition. Ce paramètre est valide uniquement pour les flux audio encodés avec le codec Windows Media Audio 9 Professional. Si ce paramètre est défini sur true, vous devez également spécifier la configuration de l’orateur de l’ordinateur client en définissant g \_ wszSpeakerConfig. |
| \_wszEnableFrameInterpolation g | **\_type WMT \_ bool**  | Si la valeur est true, le codec remet le flux vidéo à une [*fréquence d’images*](wmformat-glossary.md)supérieure, en interpolant les trames de façon algorithmique.                                                                                                                                                          |
| \_wszJustInTimeDecode g         | **\_type WMT \_ bool**  | Si la valeur est true, les données doivent être décodées le plus tard possible. Non pris en charge dans le lecteur synchrone.                                                                                                                                                                                                                            |
| \_wszNeedsPreviousSample g      | **\_type WMT \_ bool**  | Si la valeur est true, l’exemple requiert la décompression de l’exemple précédent. Ce paramètre s’applique uniquement aux images Delta dans une vidéo compressée et est en lecture seule.                                                                                                                                                                       |
| \_wszScrambledAudio g           | **\_type WMT \_ bool**  | Si la valeur est true, cette sortie utilise le schéma de masquage des erreurs audio brouillées. Il s’agit d’un paramètre valide pour les sorties audio uniquement.                                                                                                                                                                                                |
| \_wszSingleOutputBuffer g       | **\_type WMT \_ bool**  | Si la valeur est true, une seule mémoire tampon de sortie doit être utilisée (par exemple, un® de mémoire tampon vidéo de DirectDraw). Non pris en charge dans le lecteur synchrone.                                                                                                                                                                                           |
| \_wszSoftwareScaling g          | **\_type WMT \_ bool**  | Si la valeur est false, la vidéo n’est pas mise à l’échelle. (Il ne doit y avoir aucune modification de la résolution.)                                                                                                                                                                                                                                                |
| \_wszSpeakerConfig g            | **\_valeur DWORD de type WMT \_** | Si le décodage audio multicanal est activé en définissant g \_ wszEnableDiscreteOutput, ce paramètre spécifie la configuration de l’orateur de l’ordinateur client. Définissez l’une des constantes de configuration de l’orateur DirectSound.                                                                                                   |
| \_wszStreamLanguage g           | **TYPE d’un mot de passe WMT \_ \_**  | Index dans la liste de langues de la langue à remettre pour cette sortie. Utilisé pour les sorties représentant des flux qui sont mutuellement exclusifs par langue.                                                                                                                                                                      |
| \_wszVideoSampleDurations g     | **\_type WMT \_ bool**  | Si la valeur est true, le lecteur fournira des durées d’échantillonnage exactes.                                                                                                                                                                                                                                                                |
| \_wszEnableWMAProSPDIFOutput g  | **\_type WMT \_ bool**  | Si la valeur est true, le lecteur inclut le format S/PDIF de Sony/Phillips dans les types de sortie énumérés.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




