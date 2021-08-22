---
title: Vue d’ensemble du développeur
description: Vue d’ensemble du développeur
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- plug-ins Lecteur Windows Media, visualisations
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
ms.openlocfilehash: d20988a8cf1b7923699ec9cee7990b99840b8acdf9371e74da5940ddb8fc8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579411"
---
# <a name="developer-overview"></a>Vue d’ensemble du développeur

du point de vue du développeur, les visualisations sont des programmes logiciels qui prennent des données audio fournies par Lecteur Windows Media et les convertissent en graphiques qui seront les yeux de l’utilisateur. Les sujets principaux qu’un développeur doit comprendre pour créer une nouvelle visualisation sont les suivants :

## <a name="visualization-packaging"></a>Empaquetage de visualisation

les visualisations sont des contrôles COM que Lecteur Windows Media utilise pour transformer des formes d’ondes audio en graphiques animés dans Microsoft Windows. les contrôles COM sont empaquetés en tant que bibliothèques de liens dynamiques (dll) de Microsoft Windows et doivent être inscrits dans le registre Windows. lorsque Lecteur Windows Media s’exécute, les visualisations personnalisées enregistrées sont chargées et affichées conformément aux instructions de l’apparence que Lecteur Windows Media utilise.

## <a name="audio-input"></a>Entrée audio

Lecteur Windows Media fournit votre code avec des instantanés de données audio frequency et waveform à des intervalles chronométrés mesurés en fractions de seconde. l’intervalle de capture instantanée est déterminé en interne par le Lecteur Windows Media.

## <a name="graphical-output"></a>Sortie graphique

la sortie graphique de votre visualisation est un contexte de périphérique Microsoft Windows. il s’agit d’une surface de dessin Windows standard que vous pouvez dessiner à chaque fois qu’un instantané audio est fourni. toute la technologie d’Windows d’arrière-plan est prise en charge pour vous. Il vous suffit de dessiner sur le contexte de l’appareil avec les données audio fournies.

## <a name="drawing-tools"></a>Outils de dessin

vous pouvez dessiner sur le contexte de périphérique à l’aide de fonctions Microsoft Windows Graphics Device Interface (GDI) standard, en utilisant des stylets et des pinceaux pour créer des conceptions qui sont modifiées par les données audio fournies par Lecteur Windows Media. GDI fournit un ensemble complet d’outils de dessin qui peuvent créer de nombreux genres d’effets visuels.

## <a name="programming-language"></a>Langage de programmation

Microsoft Visual C++ 6,0 et versions ultérieures est la seule langue prise en charge pour la création de visualisations personnalisées.

## <a name="plug-in-wizard"></a>Assistant de plug-in

Lecteur Windows Media fournit un assistant COM que vous pouvez ajouter à Visual C++ qui générera le code sous-jacent requis pour votre visualisation. Non seulement tous les fichiers sources sont fournis, mais un exemple d’apparence est généré pour faciliter le test de votre visualisation. Le code généré crée une visualisation similaire aux barres, avec deux présélections. Vous pouvez ensuite modifier le code pour créer votre propre visualisation. un fichier de registre est également généré pour inscrire votre visualisation afin que Lecteur Windows Media puisse la charger.

La rubrique suivante décrit comment le code de visualisation traite les données audio :

-   [Flow de contrôle](flow-of-control.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des visualisations personnalisées**](about-custom-visualizations.md)
</dt> </dl>

 

 




