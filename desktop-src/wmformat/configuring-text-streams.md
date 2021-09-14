---
title: Configuration de la Flux de texte
description: Configuration de la Flux de texte
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flux, configuration de flux de texte
- codecs, configuration des flux de texte
- flux de texte, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219593"
---
# <a name="configuring-text-streams"></a>Configuration de la Flux de texte

Les flux de texte sont essentiellement les mêmes que les flux arbitraires personnalisés. Il n’y a pas d’informations de configuration associées à un flux de texte pour identifier le type d’encodage de texte, de sorte que l’objet Writer ne peut pas vérifier les exemples.

Pour configurer un flux de texte, vous devez vous assurer que la structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contient un type de média majeur de \_ texte WMMEDIATYPE. Vous devez également définir une vitesse de transmission et une fenêtre de mémoire tampon pour le flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour des Flux arbitraires**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Configuration commune à tous les Flux**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuration de types de flux arbitraires**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Flux de texte**](text-streams.md)
</dt> </dl>

 

 




