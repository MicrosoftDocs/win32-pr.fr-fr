---
title: Configuration de flux arbitraires personnalisés
description: Configuration de flux arbitraires personnalisés
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flux, configuration de flux arbitraires personnalisés
- codecs, configuration de flux arbitraires personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672974"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configuration de flux arbitraires personnalisés

Lorsque vous utilisez votre propre type de données arbitraire, vous devez créer une valeur GUID qui servira d’identificateur de type de média majeur. Lorsque l’enregistreur rencontre un flux dans un profil avec un type majeur qu’il ne reconnaît pas, il suppose que le flux de données est une donnée arbitraire personnalisée. Il acceptera vos exemples, les paquets de paquets et les combinera avec des échantillons des autres flux du fichier sans vérifier les données de quelque manière que ce soit.

Vous pouvez également créer vos propres identificateurs GUID de sous-type pour définir des sous-catégories de vos données personnalisées. L’enregistreur ignore complètement ces sous-types, mais ils sont conservés dans la section d’en-tête du fichier ASF, de sorte que votre application de lecture peut les récupérer et prendre des décisions en fonction de celles-ci.

Un flux arbitraire requiert une vitesse de transmission et une fenêtre de mémoire tampon, et doit avoir une structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) dont les valeurs sont effacées, à l’exception du type de média et du sous-type (si vous en utilisez un).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration commune à tous les flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flux de données arbitraires personnalisés**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




