---
description: Convertisseur de tee/récepteur à récepteur
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Convertisseur de tee/récepteur à récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541920"
---
# <a name="teesink-to-sink-converter"></a>Convertisseur de tee/récepteur à récepteur

Le convertisseur tee/Sink-to-Sink est un filtre en mode noyau, KsProxy. Il est utilisé dans les graphiques de filtres de télévision vidéo analogiques dans lesquels les données VBI sont rendues ou capturées. Le filtre est connecté en amont au [filtre de capture vidéo WDM](wdm-video-capture-filter.md) et constitue un moyen efficace pour dupliquer des flux de données en mode noyau sans les transitions coûteuses entre le mode noyau et le mode utilisateur. Il remet chaque bloc de données reçu à toutes les broches de sortie, et le codec en aval est chargé de rechercher les données VBI spécifiques à décoder.

Le convertisseur de tee/Sink-to-Sink apparaît dans la catégorie de filtre « périphériques de streaming WDM en t/Splitter » (AM \_ KSCATEGORY \_ Splitter).

Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md). Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 
