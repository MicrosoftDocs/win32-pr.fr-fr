---
title: Versions DRM
description: Versions DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK, versions DRM
- gestion des droits numériques (DRM), versions
- DRM (gestion des droits numériques), versions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939821"
---
# <a name="drm-versions"></a>Versions DRM

Il existe plusieurs versions de la gestion des droits numériques (DRM) Windows Media. La version 1 de la gestion des droits relatifs à l’exception est souvent différente des autres versions de cette documentation, car elle est implémentée à l’aide de techniques différentes de celles des versions ultérieures. La deuxième génération de Windows Media DRM est appelée DRM version 7, car elle a été introduite dans le cadre du kit de développement logiciel (SDK) Windows Media Format 7. Il est parfois appelé DRM version 2. Les versions ultérieures de Windows Media DRM, DRM version 9 et le nouveau Windows Media DRM 10, sont des extensions de la version 7 de DRM et utilisent les mêmes procédures pour l’implémentation. Toutes les versions de Windows Media DRM utilisent les mêmes routines de chiffrement. les différences entre les versions sont liées aux fonctionnalités de licence.

Lorsque vous créez des fichiers protégés à l’aide des objets du kit de développement logiciel (SDK) Windows Media format, vous devez prendre en charge la version 1 et la version la plus récente. Les fichiers protégés par DRM version 1 diffèrent des fichiers protégés par les versions ultérieures uniquement dans le contenu de l’en-tête. Les fichiers les plus récents qui contiennent les informations d’en-tête supplémentaires peuvent toujours être utilisés sur les clients qui affichent uniquement le contenu de la version 1. Alors que les versions ultérieures de DRM offrent un plus haut niveau de sécurité et des fonctionnalités supplémentaires, il existe toujours de nombreux lecteurs qui utilisent uniquement la version 1.

Pour plus d’informations sur les versions DRM, consultez la documentation du kit de développement logiciel (SDK) Windows Media Rights Manager.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




