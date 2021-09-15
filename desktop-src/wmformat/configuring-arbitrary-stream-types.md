---
title: Configuration de types de flux arbitraires
description: Configuration de types de flux arbitraires
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flux, configuration de types de flux arbitraires
- codecs, configuration de types de flux arbitraires
- flux, GenProfile
- codecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522116"
---
# <a name="configuring-arbitrary-stream-types"></a>Configuration de types de flux arbitraires

La plupart des types de flux arbitraires ont simplement besoin d’une vitesse de transmission, d’une fenêtre de mémoire tampon et d’un type de média majeur approprié dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Toutefois, certains types arbitraires nécessitent une configuration supplémentaire.

Si vous avez des difficultés à configurer un flux, reportez-vous à l’exemple d’application appelé GenProfile, qui est inclus dans ce kit de développement logiciel (SDK). La bibliothèque définie dans GenProfile contient le code pour l’inclusion de tous les types de flux. Pour plus d’informations sur GenProfile et les autres exemples, consultez [exemples d’applications](sample-applications.md).

Les sections suivantes décrivent comment configurer des types de flux arbitraires.



| Section                                                                                                                                        | Description                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configuration des Flux de script](configuring-script-streams.md)                                                                                   | Décrit comment configurer des flux de script.                                                  |
| [Configuration du transfert de fichiers Flux](configuring-file-transfer-streams.md)                                                                     | Décrit comment configurer des flux de transfert de fichiers.                                           |
| [Configuration de Flux Web](configuring-web-streams.md)                                                                                         | Décrit comment configurer des flux Web.                                                     |
| [Configuration de la Flux de texte](configuring-text-streams.md)                                                                                       | Décrit comment configurer des flux de texte.                                                    |
| [Configuration de Flux arbitraires personnalisés](configuring-custom-arbitrary-streams.md)                                                               | Décrit comment configurer des flux pour des types de flux arbitraires personnalisés.                       |
| [Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour des Flux arbitraires](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Décrit comment calculer la vitesse de transmission et les paramètres de fenêtre de mémoire tampon pour un flux arbitraire. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux arbitraire**](arbitrary-streams.md)
</dt> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> </dl>

 

 




