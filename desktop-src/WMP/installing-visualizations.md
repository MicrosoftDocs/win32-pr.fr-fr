---
title: Installation des visualisations
description: Installation des visualisations
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Plug-ins du lecteur Windows Media, visualisations
- plug-ins, visualisations
- visualisations, installation
- visualisations personnalisées, installation
- installation des visualisations
- visualisations, inscription
- visualisations personnalisées, inscription
- Registre, visualisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532030"
---
# <a name="installing-visualizations"></a>Installation des visualisations

Vous devez fournir un processus d’installation pour l’utilisateur de votre visualisation. Vous devez également fournir un processus de désinstallation pour l’utilisateur. La version actuelle du lecteur Windows Media n’installe pas les visualisations à partir de l’interface utilisateur.

## <a name="installing-to-the-visualization-folder"></a>Installation dans le dossier visualisation

Il est recommandé d’installer toutes les visualisations dans le sous-dossier visualisations du dossier où le lecteur Windows Media est installé.

## <a name="registering-your-visualization"></a>Inscription de votre visualisation

Les visualisations sont des DLL COM et suivent toutes les règles normales d’installation et de suppression. Vous pouvez utiliser regsvr32.exe ou d’autres outils d’installation pour inscrire votre visualisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des visualisations personnalisées**](about-custom-visualizations.md)
</dt> </dl>

 

 




