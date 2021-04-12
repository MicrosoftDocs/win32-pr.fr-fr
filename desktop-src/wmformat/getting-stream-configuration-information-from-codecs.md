---
title: Obtention d’informations de configuration de flux à partir de codecs
description: Obtention d’informations de configuration de flux à partir de codecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flux, configurations à partir de codecs
- codecs, obtention de configurations de flux à partir de
- flux, formats de codec
- codecs, formats
- flux, interface IWMCodecInfo
- IWMCodecInfo, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381677"
---
# <a name="getting-stream-configuration-information-from-codecs"></a>Obtention d’informations de configuration de flux à partir de codecs

Pour les flux audio et vidéo qui utilisent les codecs vidéo et Windows Media Audio, vous devez obtenir les valeurs des structures de configuration de flux à partir du codec que vous souhaitez utiliser. Bien qu’il soit possible de définir ces valeurs vous-même, l’utilisation des codecs garantit que les valeurs sont exactes. Vous ne devez pas modifier les valeurs de ces structures, sauf si la documentation recommande spécifiquement une modification particulière.

Les informations des codecs sont fournies sous la forme de formats de codec. Chaque format de codec est un format de flux unique pris en charge par le codec. Pour plus d’informations sur les formats de flux, consultez [formats](formats.md).

Vous pouvez demander des informations à partir des codecs Windows Media à l’aide des interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)et [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) de l’objet gestionnaire de profils. Pour obtenir l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) d’un objet de gestionnaire de profils, appelez la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Appelez **QueryInterface** sur **IWMProfileManager** pour accéder à **IWMCodecInfo3**.

Les sections suivantes décrivent l’obtention des informations dont vous avez besoin.



| Section                                                                                                | Description                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pour énumérer tous les codecs Windows Media installés](to-enumerate-all-installed-windows-media-codecs.md) | Décrit comment utiliser les méthodes des interfaces **IWMCodecInfo** et **IWMCodecInfo2** pour récupérer le nom et l’index du codec de chaque codec Windows Media installé. |
| [Pour énumérer les formats de codec](to-enumerate-codec-formats.md)                                           | Décrit comment obtenir des objets de configuration de flux à partir de codecs à utiliser dans vos profils.                                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> </dl>

 

 




