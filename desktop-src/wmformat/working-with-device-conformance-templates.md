---
title: Utilisation des modèles de conformité des appareils
description: Utilisation des modèles de conformité des appareils
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- profils, modèles de conformité des appareils
- profils, modèles de conformité
- codecs, modèles de conformité des appareils
- codecs, modèles de conformité
- modèles de conformité des appareils, à propos de
- modèles de conformité
- modèles, modèles de conformité des appareils
- ASF (Advanced Systems Format), modèles de conformité des appareils
- ASF (format des systèmes avancés), modèles de conformité des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101249"
---
# <a name="working-with-device-conformance-templates"></a>Utilisation des modèles de conformité des appareils

En raison de la grande flexibilité des fichiers ASF, il est souvent difficile de déterminer si un fichier est adapté à la lecture sur un appareil spécifique. Par exemple, les fichiers écrits pour la lecture locale sur les ordinateurs de bureau ne sont pas optimaux pour une utilisation sur des appareils mobiles. Les modèles de conformité des appareils permettent aux applications d’identifier rapidement le type d’appareil de lecture pour lequel un fichier a été conçu. Si le modèle de conformité de l’appareil ne correspond pas à l’appareil, l’application peut informer l’utilisateur que le fichier est inapproprié pour l’appareil. De cette façon, l’utilisateur peut être assuré d’une meilleure expérience de lecture.

Si vous écrivez des fichiers exclusivement pour une utilisation sur des ordinateurs personnels, les modèles de conformité des appareils ne seront pas autant d’un facteur à prendre en compte lors de la création de profils. L’objectif principal de ces modèles est de s’assurer que les fichiers créés pour une utilisation avec un matériel spécial sont compatibles avec une gamme complète d’appareils et pas seulement un appareil unique.

Un modèle de conformité des appareils est une assertion selon laquelle un fichier ASF contient des données encodées dans certains paramètres. Pour plus d’informations sur les paramètres appropriés pour les modèles individuels, consultez [paramètres de modèle de conformité des appareils](device-conformance-template-parameters.md).

Les codecs suivants prennent en charge les modèles de conformité des appareils :

-   Windows Media Video 9
-   Windows Media Audio 9 et versions ultérieures
-   Windows Media Audio 9 professionnel et versions ultérieures
-   Voix Windows Media Audio 9

Vous n’avez pas besoin de prendre des mesures spéciales pour utiliser les modèles de conformité des appareils. Le codec écrit automatiquement une chaîne de modèle pour chaque flux approprié dans le fichier. Le codec détermine le modèle à utiliser, en fonction des paramètres de configuration de flux du profil. Il existe un chevauchement des paramètres de modèle de conformité des appareils. vous pouvez donc demander un modèle spécifique au lieu de laisser le codec en affecter un pour vous. Vous pouvez spécifier le modèle de votre choix en définissant la \_ propriété g wszDecoderComplexityRequested avec les méthodes de l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) de l’objet de configuration de flux approprié.

Lors de l’écriture d’un fichier ASF, le modèle de conformité de périphérique réel pour chaque flux est défini sur la valeur transmise au writer par le codec. Lors de l’ouverture d’un fichier en lecture, vous pouvez identifier le modèle dans lequel les flux du fichier sont conformes à l’aide des méthodes de l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) pour récupérer l' \_ attribut g wszDeviceConformanceTemplate au niveau du flux. Pour plus d’informations sur les attributs, consultez [utilisation des métadonnées](working-with-metadata.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Conception de profils**](designing-profiles.md)
</dt> <dt>

[**Paramètres du modèle de conformité des appareils**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




