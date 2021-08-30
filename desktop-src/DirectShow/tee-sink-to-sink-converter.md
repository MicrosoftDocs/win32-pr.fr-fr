---
description: Convertisseur de tee/récepteur à récepteur
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertisseur de tee/récepteur à récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b1639572dc4809df4b326fabeac613bbb1b38b9392b32e1c1f54f717a0f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050009"
---
# <a name="teesink-to-sink-converter"></a>Convertisseur de tee/récepteur à récepteur

Le convertisseur tee/Sink-to-Sink est un filtre en mode noyau, KsProxy. Il est utilisé dans les graphiques de filtres de télévision vidéo analogiques dans lesquels les données VBI sont rendues ou capturées. Le filtre est connecté en amont au [filtre de capture vidéo WDM](wdm-video-capture-filter.md) et constitue un moyen efficace pour dupliquer des flux de données en mode noyau sans les transitions coûteuses entre le mode noyau et le mode utilisateur. Il remet chaque bloc de données reçu à toutes les broches de sortie, et le codec en aval est chargé de rechercher les données VBI spécifiques à décoder.

Le convertisseur de tee/Sink-to-Sink apparaît dans la catégorie de filtre « périphériques de streaming WDM en t/Splitter » (AM \_ KSCATEGORY \_ Splitter).

Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md). Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 
