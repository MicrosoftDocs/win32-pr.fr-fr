---
description: Énumération des types audio pour des modes d’encodage spécifiques
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Énumération des types audio pour des modes d’encodage spécifiques (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393268"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Énumération des types audio pour des modes d’encodage spécifiques (Microsoft Media Foundation)

Les types de média d’entrée et de sortie acceptés par l’encodeur audio sont très structurés. Vous devez obtenir les types de sortie pris en charge en appelant la méthode **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**. Une fois que vous avez obtenu un type de sortie, vous ne devez pas le modifier.

Si vous souhaitez utiliser un mode d’encodage autre qu’un passe CBR, vous devez définir le mode, puis énumérer les types de sortie pour ce mode. l’encodeur modifie les types de sortie pris en charge selon le mode défini. Les propriétés qui contrôlent le mode d’encodage sont [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) et [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md). Lorsque le mode est défini dans l’encodeur, vous devez énumérer et sélectionner un type de sortie, en l’utilisant sans modification, comme avec CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identification des types VBR basés sur la qualité

La procédure d’identification des types VBR basés sur la qualité varie selon que l’encodeur agit comme un objet de média DirectX (DMO) ou agit comme une transformation de Media Foundation (MFT). Pour plus d’informations sur le moment où un encodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).

Lorsqu’un encodeur audio fait office de DMO et que vous configurez l’encodeur pour utiliser le VBR à passage unique, il énumère tous les types de sortie pris en charge. Toutefois, vous souhaiterez généralement sélectionner un type VBR à un passage basé sur le paramètre Quality. L’encodeur place la valeur de qualité pour les types de sortie VBR à un passage dans le membre **nAvgBytesPerSec** de la structure **WAVEFORMATEX** désignée par **DMO \_ Media \_ type. pbFormat**.

Cette valeur est stockée au format suivant : 0x7FFFFFXX, où XX est la valeur de qualité (comprise entre 0 et 100). Par exemple, la valeur **nAvgBytesPerSec** de 0x7FFFFF62 spécifie le niveau de qualité 98 (0x62 = 98).

L’exemple suivant montre comment vérifier le niveau de qualité d’un format lorsque l’encodeur agit comme DMO.


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



Lorsque l’encodeur joue le rôle de MFT et qu’il énumère un type de sortie sur un appel à **GetAvailableOutputType**, vous pouvez interroger la table MFT pour la propriété **\_ \_ \_ \_ VBRQUALITY énumérée la plus récente MFPKEY** . La valeur retournée indique la qualité VBR du type de média de sortie retourné le plus récemment. Vous pouvez ensuite utiliser cette valeur pour définir la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) de l’encodeur.

## <a name="setting-peak-constraints"></a>Définition des contraintes de pointe

Pour les VBR basés sur la qualité VBR (un passage) et les deux passes sans contrainte, aucun paramètre supplémentaire n’est nécessaire après avoir récupéré le type de sortie. Pour utiliser le VBR à limite maximale, récupérez un type de sortie avec VBR activé et deux passes définies. Ce type, sans modification, décrit les paramètres VBR non restreints. Pour définir des contraintes de pointe, définissez les propriétés [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md) et [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’encodage audio](configuringaudioencoding.md)
</dt> <dt>

[Recherche de types de sortie d’encodeur audio](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Utilisation de l’encodage Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Utilisation de l’encodage VBR](usingvbrencoding.md)
</dt> </dl>

 

 



