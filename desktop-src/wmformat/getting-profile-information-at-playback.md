---
title: Obtention d’informations de profil lors de la lecture
description: Obtention d’informations de profil lors de la lecture
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, profils
- ASF (Advanced Systems Format), profils
- ASF (format des systèmes avancés), profils
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- ASF (Advanced Systems Format), partage de bande passante
- ASF (format de systèmes avancés), partage de bande passante
- flux, obtention des informations de profil lors de la lecture
- profils, obtention d’informations lors de la lecture
- exclusion mutuelle, obtention des informations de profil lors de la lecture
- partage de bande passante, obtention des informations de profil lors de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0f9386301b426adb3c4c425ac9329309c7e45146e312cc41df0bd1c453d485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839919"
---
# <a name="getting-profile-information-at-playback"></a>Obtention d’informations de profil lors de la lecture

Les informations du profil utilisé pour créer un fichier sont stockées dans la section d’en-tête du fichier. Les deux objets Reader peuvent accéder aux informations de profil à partir de l’en-tête de fichier. Il existe plusieurs raisons pour lesquelles vous pouvez souhaiter accéder aux données de profil à partir du lecteur. En règle générale, vous devez récupérer des informations sur les flux, les objets d’exclusion mutuelle et les objets de partage de bande passante.

L’objet lecteur asynchrone et l’objet lecteur synchrone peuvent être interrogés pour l’interface [**IWMProfile**](iwmprofile.md) . Aucune modification apportée aux informations de profil ne peut avoir d’incidence sur le fichier dans le lecteur. Pour plus d’informations sur l’accès aux informations de profil, consultez [utilisation des profils](working-with-profiles.md).

## <a name="stream-information"></a>Informations de flux

Il est parfois important de savoir comment un flux est configuré. Lorsque vous récupérez des propriétés de média à partir de l’un des objets Reader, vous recevez les propriétés des sorties. Les propriétés de sortie décrivent comment les données non compressées d’un flux vont être remises par le lecteur, et non la manière dont le flux est configuré dans le fichier ASF.

Lors de la réception d’exemples de flux non compressés à partir de l’un des objets Reader, vous devez utiliser les informations de profil pour identifier le format des données compressées. Cela est particulièrement important si vous envisagez d’écrire le flux compressé dans un autre fichier ASF.

Vous devez également accéder aux informations de flux lors de l’utilisation de la recompression intelligente pour transcoder un flux audio vers une vitesse de transmission inférieure.

Vous pouvez déterminer si un flux a été écrit à l’aide de l’encodage VBR (variable binaire rate). Vous ne pouvez pas accéder à des informations VBR à partir de l’interface **IWMProfile** de l’un des objets Reader. Cela est dû au fait que les informations VBR ne sont pas stockées dans le fichier après l’encodage. Vous pouvez déterminer si un flux a été créé à l’aide de l’encodage VBR en obtenant un pointeur vers l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) de l’objet lecteur et en appelant [**IWMHeaderInfo :: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). Vous devez spécifier le numéro de flux et passer g \_ wszIsVBR comme nom d’attribut.

## <a name="mutual-exclusion-information"></a>Informations d’exclusion mutuelle

Si vous souhaitez créer une application de lecture qui utilise l’exclusion mutuelle, vous devez accéder aux informations sur les objets d’exclusion mutuelle inclus dans le profil. Pour tous les types d’exclusion mutuelle, à l’exception de la vitesse de transmission, l’application de lecture est responsable des basculements de flux requis. Pour basculer entre les flux, vous devez connaître les flux.

## <a name="bandwidth-sharing-information"></a>Informations sur le partage de bande passante

Les objets de partage de bande passante inclus dans un profil sont inclus uniquement à titre d’information. Ni l’objet Writer ni l’un des deux objets Reader ne prennent d’action en raison des données de partage de bande passante. Si vous souhaitez utiliser le partage de bande passante dans votre application de lecture, vous devez accéder aux informations de partage de bande passante à partir des données de profil.

> [!Note]  
> Les informations du profil utilisé pour créer un fichier ne sont pas toutes présentes dans l’en-tête de fichier. En règle générale, les données qui sont utilisées uniquement au moment de l’encodage ne sont pas conservées dans le fichier. Cela comprend les paramètres d’entrée qui ont été définis à l’aide de la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , ainsi que les propriétés définies à l’aide de la méthode [**IWMPropertyVault :: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




