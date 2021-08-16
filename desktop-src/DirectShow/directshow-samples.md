---
description: DirectShow Extraits
ms.assetid: 4166d5ca-5e02-49f6-bcb1-d448f8175a0c
title: DirectShow Extraits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb99271821fcef80b66b379b29bd42de0505011fd47c8dfee208e6f00b007208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821164"
---
# <a name="directshow-samples"></a>DirectShow Extraits

les exemples de DirectShow sont fournis avec le [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx). Ils se trouvent sous le chemin path \[ SDK root \] \\ Samples \\ \\ DirectShow.

le tableau suivant répertorie tous les exemples de DirectShow fournis dans le SDK Windows. pour obtenir des instructions sur la façon de générer les exemples, reportez-vous à la documentation fournie dans le SDK Windows.

S’il existe une documentation supplémentaire pour un exemple, la première colonne de cette table est liée à celui-ci.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Exemple</th>
<th>Domaine</th>
<th>Description</th>
<th>Dépendances supplémentaires</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="directshow-base-classes.md">DirectShow Classes de base</a></td>
<td>Bibliothèque de classes de base</td>
<td>classes C++ et fonctions utilitaires conçues pour implémenter des filtres de DirectShow.</td>

</tr>
<tr class="even">
<td><a href="amcap-sample.md">Exemple AmCap</a></td>
<td>Capture</td>
<td>Application de capture vidéo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="dvapp-sample.md">Exemple DVApp</a></td>
<td>Capture</td>
<td>Application de capture vidéo numérique (DV).</td>

</tr>
<tr class="even">
<td><a href="playcap-sample.md">Exemple PlayCap</a></td>
<td>Capture</td>
<td>Application de capture simple.</td>

</tr>
<tr class="odd">
<td><a href="dmo-demo-sample.md">DMO Exemple de démonstration</a></td>
<td>DMO</td>
<td>Flux des données audio à partir d’un fichier WAV à l’aide d’un effet audio DMO.</td>
<td>Kit de développement logiciel (SDK) DirectX</td>
</tr>
<tr class="even">
<td>Exemple de DVD</td>
<td>DVD</td>
<td>Illustre la lecture et la navigation de base des DVD, ainsi que des fonctionnalités avancées telles que la gestion du niveau parental, les signets, le karaoké et la synchronisation des commandes.</td>

</tr>
<tr class="odd">
<td><a href="inftee-filter-sample.md">Exemple de filtre InfTee</a></td>
<td>Filtres, divers</td>
<td>Exemple d’implémentation du filtre <a href="infinite-pin-tee-filter.md">tee de code PIN infini</a> .</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="metronome-filter-sample.md">Exemple de filtre métronome</a></td>
<td>Filtres, divers</td>
<td>Montre comment implémenter une horloge de référence.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="psi-parser-filter-sample.md">Exemple de filtre de l’analyseur PSI</a></td>
<td>Filtres, divers</td>
<td>Reçoit les tables d’informations spécifiques au programme (PSI) à partir d’un flux de transport MPEG-2 et extrait les informations du programme.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dump-filter-sample.md">Exemple de filtre dump</a></td>
<td>Filtres, convertisseur</td>
<td>Écrit des exemples de médias dans un fichier texte.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Filtre SampVid</td>
<td>Filtres, convertisseur</td>
<td>Filtre de convertisseur vidéo.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="scope-filter-sample.md">Exemple de filtre d’étendue</a></td>
<td>Filtres, convertisseur</td>
<td>Affiche les données audio sous forme de formulaires Wave.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="async-filter-sample.md">Exemple de filtre Async</a></td>
<td>Filtres, source</td>
<td>Filtre de lecteur de fichier qui prend en charge le téléchargement progressif.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="ball-filter-sample.md">Exemple de filtre balle</a></td>
<td>Filtres, source</td>
<td>Filtre de source vidéo qui produit une image d’une balle rebondissante.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="push-source-filters-sample.md">Exemple de filtres de source Push</a></td>
<td>Filtres, source</td>
<td>Filtres sources qui fournissent les données suivantes sous la forme d’un flux vidéo : une image bitmap unique, un ensemble de bitmaps, une copie de l’image de bureau actuelle.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="synth-filter-sample.md">Exemple de filtre Synth</a></td>
<td>Filtres, source</td>
<td>Filtre source qui génère des formes d’ondes audio. Cet exemple illustre la génération de graphiques dynamiques.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="ezrgb24-filter-sample.md">Exemple de filtre EZRGB24</a></td>
<td>Filtres, transformer</td>
<td>Filtre de traitement d’image.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="gargle-filter-sample.md">Exemple de filtre gargle</a></td>
<td>Filtres, transformer</td>
<td>Filtre d’effet audio.</td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td><a href="wavdest-filter-sample.md">Exemple de filtre WavDest</a></td>
<td>Filtres, transformer</td>
<td>Écrit un flux audio dans un fichier WAV.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td><a href="dmoenum-sample.md">Exemple DMOEnum</a></td>
<td>Divers</td>
<td>Montre comment énumérer les <a href="directx-media-objects.md">objets DMOs (DirectX Media Objects</a> ).</td>

</tr>
<tr class="odd">
<td><a href="mapper-sample.md">Exemple de Mappeur</a></td>
<td>Divers</td>
<td>Montre comment utiliser le <a href="filter-mapper.md">Mappeur de filtre</a> pour rechercher des filtres dans le registre.</td>

</tr>
<tr class="even">
<td>Exemple SysEnum</td>
<td>Divers</td>
<td>Montre comment utiliser l' <a href="system-device-enumerator.md">énumérateur de périphérique système</a> pour énumérer des appareils et des filtres.</td>

</tr>
<tr class="odd">
<td><a href="cutscene-sample.md">Exemple CutScene</a></td>
<td>Lecture</td>
<td>Lit un fichier vidéo en mode plein écran.</td>

</tr>
<tr class="even">
<td>Exemple DDrawXCL</td>
<td>Lecture</td>
<td>lit la vidéo en mode plein écran en mode plein écran DirectDraw, à l’aide de l’interface <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a> sur le filtre de <a href="overlay-mixer-filter.md">Mixer de superposition</a> .</td>

</tr>
<tr class="odd">
<td>Exemple DShowPlayer</td>
<td>Lecture</td>
<td>Application de lecture vidéo.</td>

</tr>
<tr class="even">
<td>Exemple EVRPlayer</td>
<td>Lecture</td>
<td>montre comment utiliser le filtre DirectShow EVR.
<blockquote>
[!Note]<br />
requiert Windows Vista ou version ultérieure.
</blockquote>
<br/> <br/> cet exemple est disponible dans le SDK Windows pour Windows Server 2008 ou version ultérieure.<br/></td>
<td>strmbase. lib</td>
</tr>
<tr class="odd">
<td>Exemple Texture3D9</td>
<td>Lecture</td>
<td>Dessine une vidéo sur une surface de texture Microsoft DirectX 9,0.</td>
<td>strmbase. lib, SDK DirectX</td>
</tr>
<tr class="even">
<td><a href="ticker-sample.md">Exemple de ticker</a></td>
<td>VMR-9</td>
<td>Utilise VMR-9 pour fusionner la vidéo et le texte.</td>

</tr>
<tr class="odd">
<td>Exemple VMR9Allocator</td>
<td>VMR-9</td>
<td>Implémente un Allocator-Presenter personnalisé pour VMR-9.</td>
<td>strmbase. lib</td>
</tr>
<tr class="even">
<td>Exemple VMR9Compositor</td>
<td>VMR-9</td>
<td>Implémente un mélangeur personnalisé pour VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="vmrplayer-sample.md">Exemple VMRPlayer</a></td>
<td>VMR-9</td>
<td>Utilise VMR-9 pour fusionner une ou deux vidéos en cours d’exécution et une image statique.</td>

</tr>
<tr class="even">
<td>Exemple de filigrane</td>
<td>VMR-9</td>
<td>Fusionne une image bitmap statique sur une vidéo pendant la lecture, à l’aide de VMR-9.</td>

</tr>
<tr class="odd">
<td><a href="windowless-sample.md">Exemple sans fenêtre</a></td>
<td>VMR-9</td>
<td>Illustre le mode sans fenêtre dans VMR-9.</td>

</tr>
</tbody>
</table>



 

## <a name="additional-dependencies"></a>Dépendances supplémentaires

certains des exemples sont liés à la bibliothèque de classes de base DirectShow. Pour générer ces exemples, vous devez d’abord créer la bibliothèque de classes de base. pour plus d’informations, consultez [DirectShow les Classes de Base](directshow-base-classes.md). La bibliothèque de classes de base est requise pour tous les exemples de filtres.

certains des exemples requièrent également le kit de développement logiciel (SDK) DirectX, en plus des SDK Windows. Pour générer ces exemples, vous devez installer le kit de développement logiciel (SDK) DirectX et définir la \_ variable d’environnement% DXSDK dir% comme étant égale à votre chemin d’installation du SDK DirectX.

la plupart des exemples de DirectShow utilisent un ensemble d’en-têtes et de fichiers sources communs situés dans le \[ kit de développement logiciel (SDK) d' \] \\ exemples directrory \\ \\ DirectShow \\ commun. Si vous copiez un dossier d’exemple dans un autre répertoire, veillez à copier également le dossier commun.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’environnement de génération](setting-up-the-build-environment.md)
</dt> </dl>

 

 




