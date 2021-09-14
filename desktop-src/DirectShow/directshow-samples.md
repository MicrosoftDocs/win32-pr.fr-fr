---
description: DirectShow Extraits
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Extraits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87687905d53f91339202af2b08bffa79902e100d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006624"
---
# <a name="directshow-samples"></a>DirectShow Extraits

les exemples de DirectShow sont fournis avec le [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx). Ils se trouvent sous le chemin path \[ SDK root \] \\ Samples \\ \\ DirectShow.

le tableau suivant répertorie tous les exemples de DirectShow fournis dans le SDK Windows. pour obtenir des instructions sur la façon de générer les exemples, reportez-vous à la documentation fournie dans le SDK Windows.

S’il existe une documentation supplémentaire pour un exemple, la première colonne de cette table est liée à celui-ci.




| Exemple | Domaine | Description | Dépendances supplémentaires | 
|--------|------|-------------|-------------------------|
| <a href="directshow-base-classes.md">DirectShow Classes de base</a> | Bibliothèque de classes de base | classes C++ et fonctions utilitaires conçues pour implémenter des filtres de DirectShow. | 
| <a href="amcap-sample.md">Exemple AmCap</a> | Capture | Application de capture vidéo. | strmbase. lib | 
| <a href="dvapp-sample.md">Exemple DVApp</a> | Capture | Application de capture vidéo numérique (DV). | 
| <a href="playcap-sample.md">Exemple PlayCap</a> | Capture | Application de capture simple. | 
| <a href="dmo-demo-sample.md">DMO Exemple de démonstration</a> | DMO | Flux des données audio à partir d’un fichier WAV à l’aide d’un effet audio DMO. | Kit de développement logiciel (SDK) DirectX | 
| Exemple de DVD | DVD | Illustre la lecture et la navigation de base des DVD, ainsi que des fonctionnalités avancées telles que la gestion du niveau parental, les signets, le karaoké et la synchronisation des commandes. | 
| <a href="inftee-filter-sample.md">Exemple de filtre InfTee</a> | Filtres, divers | Exemple d’implémentation du filtre <a href="infinite-pin-tee-filter.md">tee de code PIN infini</a> . | strmbase. lib | 
| <a href="metronome-filter-sample.md">Exemple de filtre métronome</a> | Filtres, divers | Montre comment implémenter une horloge de référence. | strmbase. lib | 
| <a href="psi-parser-filter-sample.md">Exemple de filtre de l’analyseur PSI</a> | Filtres, divers | Reçoit les tables d’informations spécifiques au programme (PSI) à partir d’un flux de transport MPEG-2 et extrait les informations du programme. | strmbase. lib | 
| <a href="dump-filter-sample.md">Exemple de filtre dump</a> | Filtres, convertisseur | Écrit des exemples de médias dans un fichier texte. | strmbase. lib | 
| Filtre SampVid | Filtres, convertisseur | Filtre de convertisseur vidéo. | strmbase. lib | 
| <a href="scope-filter-sample.md">Exemple de filtre d’étendue</a> | Filtres, convertisseur | Affiche les données audio sous forme de formulaires Wave. | strmbase. lib | 
| <a href="async-filter-sample.md">Exemple de filtre Async</a> | Filtres, source | Filtre de lecteur de fichier qui prend en charge le téléchargement progressif. | strmbase. lib | 
| <a href="ball-filter-sample.md">Exemple de filtre balle</a> | Filtres, source | Filtre de source vidéo qui produit une image d’une balle rebondissante. | strmbase. lib | 
| <a href="push-source-filters-sample.md">Exemple de filtres de source Push</a> | Filtres, source | Filtres sources qui fournissent les données suivantes sous la forme d’un flux vidéo : une image bitmap unique, un ensemble de bitmaps, une copie de l’image de bureau actuelle. | strmbase. lib | 
| <a href="synth-filter-sample.md">Exemple de filtre Synth</a> | Filtres, source | Filtre source qui génère des formes d’ondes audio. Cet exemple illustre la génération de graphiques dynamiques. | strmbase. lib | 
| <a href="ezrgb24-filter-sample.md">Exemple de filtre EZRGB24</a> | Filtres, transformer | Filtre de traitement d’image. | strmbase. lib | 
| <a href="gargle-filter-sample.md">Exemple de filtre gargle</a> | Filtres, transformer | Filtre d’effet audio. | strmbase. lib | 
| <a href="wavdest-filter-sample.md">Exemple de filtre WavDest</a> | Filtres, transformer | Écrit un flux audio dans un fichier WAV. | strmbase. lib | 
| <a href="dmoenum-sample.md">Exemple DMOEnum</a> | Divers | Montre comment énumérer les <a href="directx-media-objects.md">objets DMOs (DirectX Media Objects</a> ). | 
| <a href="mapper-sample.md">Exemple de Mappeur</a> | Divers | Montre comment utiliser le <a href="filter-mapper.md">Mappeur de filtre</a> pour rechercher des filtres dans le registre. | 
| Exemple SysEnum | Divers | Montre comment utiliser l' <a href="system-device-enumerator.md">énumérateur de périphérique système</a> pour énumérer des appareils et des filtres. | 
| <a href="cutscene-sample.md">Exemple CutScene</a> | Lecture | Lit un fichier vidéo en mode plein écran. | 
| Exemple DDrawXCL | Lecture | lit la vidéo en mode plein écran en mode plein écran DirectDraw, à l’aide de l’interface <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> sur le filtre de <a href="overlay-mixer-filter.md">Mixer de superposition</a> . | 
| Exemple DShowPlayer | Lecture | Application de lecture vidéo. | 
| Exemple EVRPlayer | Lecture | montre comment utiliser le filtre DirectShow EVR.<blockquote>[!Note]<br />requiert Windows Vista ou version ultérieure.</blockquote><br /><br /> cet exemple est disponible dans le SDK Windows pour Windows Server 2008 ou version ultérieure.<br /> | strmbase. lib | 
| Exemple Texture3D9 | Lecture | Dessine une vidéo sur une surface de texture Microsoft DirectX 9,0. | strmbase. lib, SDK DirectX | 
| <a href="ticker-sample.md">Exemple de ticker</a> | VMR-9 | Utilise VMR-9 pour fusionner la vidéo et le texte. | 
| Exemple VMR9Allocator | VMR-9 | Implémente un Allocator-Presenter personnalisé pour VMR-9. | strmbase. lib | 
| Exemple VMR9Compositor | VMR-9 | Implémente un mélangeur personnalisé pour VMR-9. | 
| <a href="vmrplayer-sample.md">Exemple VMRPlayer</a> | VMR-9 | Utilise VMR-9 pour fusionner une ou deux vidéos en cours d’exécution et une image statique. | 
| Exemple de filigrane | VMR-9 | Fusionne une image bitmap statique sur une vidéo pendant la lecture, à l’aide de VMR-9. | 
| <a href="windowless-sample.md">Exemple sans fenêtre</a> | VMR-9 | Illustre le mode sans fenêtre dans VMR-9. | 




 

## <a name="additional-dependencies"></a>Dépendances supplémentaires

certains des exemples sont liés à la bibliothèque de classes de base DirectShow. Pour générer ces exemples, vous devez d’abord créer la bibliothèque de classes de base. pour plus d’informations, consultez [DirectShow les Classes de Base](directshow-base-classes.md). La bibliothèque de classes de base est requise pour tous les exemples de filtres.

certains des exemples requièrent également le kit de développement logiciel (SDK) DirectX, en plus des SDK Windows. Pour générer ces exemples, vous devez installer le kit de développement logiciel (SDK) DirectX et définir la \_ variable d’environnement% DXSDK dir% comme étant égale à votre chemin d’installation du SDK DirectX.

la plupart des exemples de DirectShow utilisent un ensemble d’en-têtes et de fichiers sources communs situés dans le \[ kit de développement logiciel (SDK) d' \] \\ exemples directrory \\ \\ DirectShow \\ commun. Si vous copiez un dossier d’exemple dans un autre répertoire, veillez à copier également le dossier commun.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’environnement de génération](setting-up-the-build-environment.md)
</dt> </dl>

 

 




