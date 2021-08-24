---
title: Assigner des formats de sortie
description: Assigner des formats de sortie
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, assigner des formats de sortie
- ASF (Advanced Systems Format), assigner des formats de sortie
- ASF (format des systèmes avancés), assigner des formats de sortie
- ASF (Advanced Systems Format), nombres et formats de sortie
- ASF (format des systèmes avancés), nombres et formats de sortie
- nombres et formats de sortie, affectation
- codecs, nombres et formats de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80672419a032b2fff779259ffc6dcebfbe9e9a569f9d4b7afbb75ae5a84fac2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659369"
---
# <a name="assigning-output-formats"></a>Assigner des formats de sortie

Certains codecs peuvent décompresser les données multimédias numériques dans plusieurs formats non compressés. Vous pouvez rechercher tous les formats pris en charge pour une sortie spécifique à l’aide du lecteur asynchrone ou du lecteur synchrone.

Pour examiner tous les formats disponibles pour une sortie, procédez comme suit. Ces procédures sont identiques pour le lecteur asynchrone et le lecteur synchrone. Lorsque les noms d’interface varient, les méthodes de lecture synchrone sont répertoriées entre parenthèses après les méthodes du lecteur asynchrone.

1.  Créez un objet lecteur et chargez un fichier pour la lecture. Pour plus d’informations, consultez [pour créer un lecteur et ouvrir un fichier](to-create-a-reader-and-open-a-file.md) (ou [pour créer un lecteur synchrone et ouvrir un fichier](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Déterminez la sortie pour laquelle vous souhaitez rechercher les formats disponibles. Si vous ne connaissez pas encore la sortie que vous souhaitez utiliser, vous pouvez identifier les sorties dans le fichier à l’aide des procédures décrites dans [pour identifier les numéros de sortie](to-identify-output-numbers.md).
3.  Récupérez le nombre total de formats disponibles pour la sortie souhaitée en appelant [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (ou [**IWMSyncReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Parcourez les formats disponibles l’un après l’autre, en effectuant les étapes suivantes pour chacun d’entre eux :
    -   Récupérez l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) pour le format de sortie actuel en appelant [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (ou [**IWMSyncReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).
    -   Récupérez la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le format de sortie en effectuant deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Effectuez le premier appel pour obtenir la taille de la structure, puis allouez de la mémoire pour celle-ci et transmettez un pointeur vers la mémoire allouée sur le deuxième appel.
    -   Recherchez le sous-type de média du format de sortie dans **WM \_ Media \_ type. SubType**.
    -   Pour la vidéo, si le sous-type actuel est le format que vous souhaitez utiliser pour la sortie, quittez la boucle. Sinon, passez à l’itération suivante.

        Pour l’audio, vous devez vérifier les valeurs de la structure **WAVEFORMATEX** en fonction de vos besoins. **WM \_ MEDIA \_ type. pbFormat** pointe vers la structure **WAVEFORMATEX** pour les sorties audio.

5.  Une fois que vous avez trouvé la sortie souhaitée, définissez-la pour l’utiliser avec le lecteur en appelant [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (ou [**IWMSyncReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). Vous devez passer un pointeur vers l’interface **IWMOutputMediaProps** obtenue à la première étape de la boucle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Utilisation des sorties**](working-with-outputs.md)
</dt> </dl>

 

 




