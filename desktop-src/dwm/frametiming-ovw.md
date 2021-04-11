---
title: Accès et contrôle des données de frame DWM
description: Cette rubrique décrit les API Gestionnaire de fenêtrage (DWM) utilisées pour la planification et la présentation multimédia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Gestionnaire de fenêtrage (DWM), planification et API de présentation multimédia
- DWM (Gestionnaire de fenêtrage), planification et API de présentation multimédia
- API de planification et de présentation multimédia
- Gestionnaire de fenêtrage (DWM), accéder aux données de frame
- DWM (Gestionnaire de fenêtrage), accéder aux données de frame
- accès aux données de frame
- Gestionnaire de fenêtrage (DWM), contrôle des données de frame
- DWM (Gestionnaire de fenêtrage), contrôle des données de frame
- contrôle des données de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310181"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Accès et contrôle des données de frame DWM

Cette rubrique décrit les API Gestionnaire de fenêtrage (DWM) utilisées pour la planification et la présentation multimédia.

## <a name="dwm-frame-timing-api"></a>API de minutage des frames DWM

Les API de planification et de présentation multimédia permettent de contrôler plus en détail le moment où l’image de bureau est composite et présentée. Cela est généralement nécessaire pour les applications de lecture vidéo et de média pour lesquelles le DWM s’exécute de façon asynchrone avec leur propre planification de présentation, ce qui peut entraîner des artefacts d’échantillonnage s’ils ne sont pas étroitement contrôlés.

Les fonctions de planification et de présentation multimédia sont les suivantes. Les détails de leur utilisation se trouvent sur ces pages.

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Notifie le DWM d’activer la planification de service de planification de classe multimédia (MMCSS) pendant que le processus appelant est actif.
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Récupère les informations de minutage de la composition actuelle.
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Modifie le nombre d’actualisations pendant lesquelles le frame précédent s’affiche.
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Définit le nombre d’actualisations dans lesquelles afficher le frame présenté.
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Définit les paramètres présents pour la composition de frame.

 

 




