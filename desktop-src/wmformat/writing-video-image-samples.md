---
title: Écriture d’exemples d’images vidéo
description: Écriture d’exemples d’images vidéo
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- ASF (Advanced Systems Format), écriture d’exemples d’images vidéo
- ASF (format des systèmes avancés), écriture d’exemples d’images vidéo
- images vidéo, exemples d’écriture
- flux, écriture d’exemples d’images vidéo
- codecs, écriture d’exemples d’images vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c05bbcc9239eede97f4ea7ca0df34004b1fb7facc0c36c8f38098c42e86fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704819"
---
# <a name="writing-video-image-samples"></a>Écriture d’exemples d’images vidéo

Un flux d’image vidéo est une vidéo qui contient une série d’images fixes. Les images peuvent se déplacer dans le frame, et chaque image peut être fusionnée dans la suivante. les flux d’images vidéo sont encodés à l’aide du codec Windows Media Video 9 image v2. la vidéo de sortie est similaire à celle créée par le codec Windows Media Video 9.

Pour créer un profil contenant un flux d’image vidéo, commencez par énumérer les codecs vidéo comme décrit dans [obtention d’informations de configuration du flux à partir de codecs](getting-stream-configuration-information-from-codecs.md). Recherchez le codec qui prend en charge le \_ sous-type WMMEDIASUBTYPE WVP2.

Après avoir défini le profil sur l’objet Writer, appelez [**IWMWriter :: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) pour obtenir les propriétés de média pour le flux d’entrée d’image vidéo. Récupérez le type de média à partir de l’objet de propriétés de média en appelant [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), puis remplacez le sous-type par WMMEDIASUBTYPE \_ VIDEOIMAGE. Vous devez définir la largeur et la hauteur de la vidéo sur les dimensions maximales requises pour englober les images que vous allez ajouter au flux. Appelez ensuite [**IWMMediaProps :: SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) avec le type d’entrée modifié. Vous êtes maintenant prêt à commencer à envoyer des exemples à l’objet Writer.

Chaque échantillon doit commencer par une **structure \_ VIDEOIMAGE \_ SAMPLE2 WMT** . En outre, les exemples peuvent contenir des images bitmap. Une image est attachée uniquement à un échantillon pour le premier frame dans lequel elle apparaît. Tous les frames supplémentaires qui utilisent cette image n’ont besoin que d’informations dans la structure. Les bitmaps d’entrée doivent être au format RVB, 24 bits par pixel.

Les fichiers bitmap stockent les données de l’image afin que les données de chaque ligne de l’image prennent un nombre d’octets divisible par quatre. (Il s’agit de la méthode STRIDE de l’image bitmap.) Cela force le début de chaque ligne de vidéo à une limite **DWORD** , ce qui rend la copie plus efficace. Si les lignes de l’image ne sont pas divisibles par quatre, la ligne est remplie au multiple le plus élevé suivant de quatre octets. Lorsque vous attachez des données image, vous devez supprimer tous les remplissages qui existent à la fin des données pour chaque ligne.

le codec Windows Media Video 9 Image v2 gère jusqu’à deux images en mémoire à la fois. Ces images sont appelées l’image précédente et l’image actuelle. Chaque image possède un ensemble de membres dans la **structure \_ VIDEOIMAGE WMT \_ SAMPLE2** , qui détermine la façon dont l’image est présentée dans le frame. Vous pouvez ajouter une image en définissant le membre dwControlFlags de **WMT \_ VIDEOIMAGE \_ SAMPLE2** sur WMT \_ VIDEOIMAGE exemple de \_ \_ Frame d’entrée \_ . Lorsque vous transmettez une trame d’entrée au codec, cette image devient l’image actuelle. L’image qui était l’image actuelle dans l’exemple précédent devient généralement l’image précédente, et l’image qui était l’image précédente dans l’exemple précédent est ignorée. Vous pouvez configurer le codec pour conserver l’ancienne image précédente en affectant la **valeur true** au membre **bKeepPrevImage** . Dans ce cas, l’image qui était l’image actuelle dans l’exemple précédent est ignorée.

La composition de base d’une image vidéo est déterminée par deux facteurs pour chaque image : la région d’intérêt et le coefficient de fusion. La région d’intérêt d’une image est définie par un point d’origine, une largeur et une hauteur. La partie d’une image décrite par la région d’intérêt remplit le frame de sortie. Si la taille de la zone d’intérêt est différente de celle de la trame de sortie, le codec le redimensionne. Le coefficient de fusion de l’image détermine la fusion des deux images. Les coefficients de fusion pour les images actuelles et précédentes doivent être au total de 1,0. Par exemple, si **fCurrBlendCoef** est défini sur 0,5 et **fPrevBlendCoef** sur 0,5, alors le frame de sortie est composé d’une fusion égale des régions d’intérêt des deux images.

En manipulant la zone d’intérêt d’une image, vous pouvez créer des effets de panoramique et de zoom. Les coefficients de fusion vous permettent d’effectuer un fondu croisé (dissoudre) entre les images. En plus de ces effets, vous pouvez utiliser l’une des transitions prédéfinies pour créer des frames plus complexes. Les transitions disponibles sont décrites dans la section [transitions d’images vidéo](video-image-transitions.md) de cette documentation. Lorsque vous utilisez une transition, vous devez configurer chaque frame. Le moyen le plus simple de procéder consiste à créer une fonction qui change de façon incrémentielle les membres de la structure VIDEOIMAGE de la **\_ \_ SAMPLE2 WMT** pour obtenir un effet complet.

Pour plus d’informations sur les valeurs à définir pour les déformations, consultez [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Remarque** Si vous souhaitez inclure des données audio dans un fichier avec un flux d’image vidéo, vous devez utiliser une entrée audio non compressée. Pour combiner un flux d’image vidéo avec un flux audio compressé existant, vous devez décompresser l’audio et passer les exemples en non compressé. Si vous transmettez des échantillons compressés à l’enregistreur lors de l’écriture d’un flux d’image vidéo, une erreur se produit, ce qui entraîne la suppression des échantillons de la vidéo.

en outre, les fichiers Image vidéo compressés sans flux audio peuvent contenir plusieurs images vidéo très petites et très compressées dans un paquet ASF unique, ce qui peut entraîner une mauvaise expérience de lecture dans les versions précédentes de Lecteur Windows Media. Pour éviter ce problème, la meilleure solution consiste à insérer un flux audio silencieux dans le fichier, bien que cela augmente également la taille du fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Image vidéo**](video-image.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




