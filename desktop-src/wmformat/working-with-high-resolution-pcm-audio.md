---
title: Utilisation d' High-Resolution audio PCM
description: Utilisation d' High-Resolution audio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), audio PCM haute résolution
- ASF (format de systèmes avancés), audio PCM haute résolution
- profils, audio PCM haute résolution
- codecs, audio PCM haute résolution
- ASF (Advanced Systems Format), audio PCM
- ASF (format des systèmes avancés), audio PCM
- profils, audio PCM
- codecs, audio PCM
- audio PCM haute résolution
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941106"
---
# <a name="working-with-high-resolution-pcm-audio"></a>Utilisation d' High-Resolution audio PCM

Certains des formats d’entrée pour le codec Windows Media Audio 9 Professional et le codec Windows Media Audio 9 Lossless sont des formats PCM haute résolution. Il s’agit de formats PCM qui ont plus de deux canaux, ou plus de 16 bits par échantillon (l’audio avec plus de deux canaux est également appelé audio multicanal).

Ces formats sont configurés à l’aide d’une extension structurée de la structure [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , appelée [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)). La structure **WAVEFORMATEXTENSIBLE** inclut des informations sur les canaux inclus dans l’audio. Cette structure est requise lors de l’utilisation de l’audio PCM haute résolution, car certaines API Windows n’acceptent pas les structures **WAVEFORMATEX** qui contiennent des valeurs haute résolution.

Les formats PCM haute résolution comportent 22 octets de données étendues, qui sont spécifiées dans le membre **cbSize** de la structure **WAVEFORMATEX** . Les formats audio Windows Media haute résolution n’utilisent pas la structure **WAVEFORMATEXTENSIBLE** , mais les données étendues sont ajoutées à la structure **WAVEFORMATEX** .

Les codecs audio Windows Media prennent uniquement en charge le décodage des formats PCM haute résolution lorsque l’application s’exécute sur Windows XP ou version ultérieure. Dans les versions antérieures de Microsoft Windows, les codecs décodent dans un format avec un maximum de 16 bits par échantillon et de 2 canaux. En outre, vous devez spécifier que le codec doit être décodé en PCM haute définition en affectant la \_ **valeur true** au paramètre de sortie g wszEnableDiscreteOutput à l’aide de la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Après avoir effectué cet appel, les sorties énumérées par le lecteur incluent des formats de haute définition.

L’audio multicanal nécessite davantage de configuration. Pour plus d’informations, consultez lecture de l' [audio multicanal](reading-multichannel-audio.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> </dl>

 

 