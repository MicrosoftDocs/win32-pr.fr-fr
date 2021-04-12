---
title: Vue d’ensemble du développeur
description: Vue d’ensemble du développeur
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-ins du lecteur Windows Media, visualisations
- plug-ins, visualisations
- visualisations, vue d’ensemble du développeur
- visualisations personnalisées, vue d’ensemble du développeur
- visualisations, contrôles COM
- visualisations personnalisées, contrôles COM
- visualisations, entrée audio
- visualisations personnalisées, entrée audio
- visualisations, sortie graphique
- visualisations personnalisées, sortie graphique
- visualisations, outils de dessin
- visualisations personnalisées, outils de dessin
- visualisations, langage de programmation
- visualisations personnalisées, langage de programmation
- visualisations, Visual C++
- visualisations personnalisées, Visual C++
- visualisations, Assistant de plug-in
- visualisations personnalisées, Assistant de plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310598"
---
# <a name="developer-overview"></a>Vue d’ensemble du développeur

Du point de vue du développeur, les visualisations sont des programmes logiciels qui prennent des données audio fournies par le lecteur Windows Media et convertissent ces données en graphiques qui seront les yeux de l’utilisateur. Les sujets principaux qu’un développeur doit comprendre pour créer une nouvelle visualisation sont les suivants :

## <a name="visualization-packaging"></a>Empaquetage de visualisation

Les visualisations sont des contrôles COM utilisés par le lecteur Windows Media pour transformer les formes d’ondes audio en graphiques animés dans Microsoft Windows. Les contrôles COM sont empaquetés en tant que bibliothèques de liens dynamiques (dll) Microsoft Windows et doivent être inscrits dans le Registre Windows. Lors de l’exécution du lecteur Windows Media, les visualisations personnalisées enregistrées sont chargées et affichées conformément aux instructions de la peau utilisée par le lecteur Windows Media.

## <a name="audio-input"></a>Entrée audio

Le lecteur Windows Media fournit votre code avec des instantanés de données audio Frequency et Waveform à des intervalles chronométrés mesurés en fractions de seconde. L’intervalle de capture instantanée est déterminé en interne par le lecteur Windows Media.

## <a name="graphical-output"></a>Sortie graphique

La sortie graphique de votre visualisation est un contexte de périphérique Microsoft Windows. Il s’agit d’une surface de dessin Windows standard que vous pouvez dessiner à chaque fois qu’un instantané audio est fourni. Toutes les technologies Windows en arrière-plan sont prises en charge pour vous. Il vous suffit de dessiner sur le contexte de l’appareil avec les données audio fournies.

## <a name="drawing-tools"></a>Outils de dessin

Vous pouvez dessiner sur le contexte de périphérique à l’aide de fonctions Microsoft Windows Graphics Device Interface (GDI) standard, en utilisant des stylets et des pinceaux pour créer des conceptions qui sont modifiées par les données audio fournies par le lecteur Windows Media. GDI fournit un ensemble complet d’outils de dessin qui peuvent créer de nombreux genres d’effets visuels.

## <a name="programming-language"></a>Langage de programmation

Microsoft Visual C++ 6,0 et versions ultérieures est la seule langue prise en charge pour la création de visualisations personnalisées.

## <a name="plug-in-wizard"></a>Assistant de plug-in

Le lecteur Windows Media fournit un Assistant COM que vous pouvez ajouter à Visual C++ qui générera le code sous-jacent requis pour votre visualisation. Non seulement tous les fichiers sources sont fournis, mais un exemple d’apparence est généré pour faciliter le test de votre visualisation. Le code généré crée une visualisation similaire aux barres, avec deux présélections. Vous pouvez ensuite modifier le code pour créer votre propre visualisation. Un fichier de Registre est également généré pour inscrire votre visualisation afin que le lecteur Windows Media puisse la charger.

La rubrique suivante décrit comment le code de visualisation traite les données audio :

-   [Flow de contrôle](flow-of-control.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des visualisations personnalisées**](about-custom-visualizations.md)
</dt> </dl>

 

 




