---
title: Installation des visualisations
description: Installation des visualisations
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- plug-ins Lecteur Windows Media, visualisations
- plug-ins, visualisations
- visualisations, installation
- visualisations personnalisées, installation
- installation des visualisations
- visualisations, inscription
- visualisations personnalisées, inscription
- Registre, visualisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e36a13dae64857143a4d7a2edc4ece719164c3dc30dc8f21f907e2080a5afae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135522"
---
# <a name="installing-visualizations"></a>Installation des visualisations

Vous devez fournir un processus d’installation pour l’utilisateur de votre visualisation. Vous devez également fournir un processus de désinstallation pour l’utilisateur. la version actuelle de Lecteur Windows Media n’installe pas les visualisations à partir de l’interface utilisateur.

## <a name="installing-to-the-visualization-folder"></a>Installation dans le dossier visualisation

il est recommandé d’installer toutes les visualisations dans le sous-dossier visualisations du dossier où Lecteur Windows Media est installé.

## <a name="registering-your-visualization"></a>Inscription de votre visualisation

Les visualisations sont des DLL COM et suivent toutes les règles normales d’installation et de suppression. Vous pouvez utiliser regsvr32.exe ou d’autres outils d’installation pour inscrire votre visualisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des visualisations personnalisées**](about-custom-visualizations.md)
</dt> </dl>

 

 




