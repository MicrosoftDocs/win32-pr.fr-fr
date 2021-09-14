---
description: Création d’un Graph de capture audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Création d’un Graph de capture audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006683"
---
# <a name="creating-an-audio-capture-graph"></a>Création d’un Graph de capture audio

La première étape pour une application de capture audio consiste à créer un graphique de filtre. La configuration du graphique dépend du type de fichier que vous souhaitez créer.

-   Fichier AVI audio uniquement : filtre de capture audio vers un filtre [multiplex MUX](avi-mux-filter.md) et le filtre AVI MUX en [writer de fichier](file-writer-filter.md) .
-   Fichier WAV : filtre de capture audio de l' [exemple de filtre Wavdest](wavdest-filter-sample.md) au filtre de writer de fichier
-   Windows Fichier audio multimédia (. WMA) : filtre de capture audio pour le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) .

Le filtre WavDest est fourni en tant qu’exemple du kit de développement logiciel (SDK). Pour l’utiliser, vous devez générer et inscrire le filtre.

pour utiliser le filtre de l’enregistreur ASF, vous devez installer le kit de développement logiciel (SDK) Windows Media et obtenir une clé logicielle pour déverrouiller le filtre. pour plus d’informations, consultez [utilisation du média Windows dans DirectShow](using-windows-media-in-directshow.md).

vous pouvez générer le graphique de filtre à l’aide de l’objet [capturer Graph générateur](capture-graph-builder.md) , ou vous pouvez générer le graphique « manuellement ». autrement dit, l’application doit-elle ajouter et connecter chaque filtre par programmation. Cet article décrit l’approche manuelle. pour plus d’informations sur l’utilisation du générateur de Graph de capture, consultez [capture vidéo](video-capture.md). La plupart des informations contenues dans cet article s’appliquent aux graphiques audio uniquement.

Ajout du périphérique de capture audio

Étant donné que le filtre de capture audio communique avec un périphérique matériel spécifique, vous ne pouvez pas simplement appeler **CoCreateInstance** pour créer le filtre. Utilisez plutôt l' [énumérateur de périphérique système](system-device-enumerator.md) pour énumérer tous les appareils dans la catégorie « sources de capture audio », qui est identifiée par l’identificateur de classe CLSID \_ AudioInputDeviceCategory.

L’énumérateur de périphérique système retourne la liste des monikers pour les appareils ; le nom convivial de chaque moniker correspond au nom de l’appareil. Choisissez l’un des monikers retournés et utilisez-le pour créer une instance du filtre de capture audio pour cet appareil. Ajoutez le filtre au graphique de filtre. L’appareil d’enregistrement audio préféré de l’utilisateur apparaît en premier dans la liste moniker. (L’utilisateur sélectionne un appareil par défaut en cliquant sur sons et multimédia dans le panneau de configuration.)

Pour plus d’informations, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md).

Pour spécifier l’entrée à partir de laquelle effectuer la capture, obtenez l’interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) à partir du filtre de capture audio et appelez la méthode **put \_ Enable** pour spécifier l’entrée. Toutefois, une limitation de cette méthode est que différents périphériques matériels peuvent utiliser des chaînes différentes pour identifier leurs entrées. Par exemple, une carte peut utiliser le « microphone » pour identifier l’entrée microphone et une autre carte peut utiliser « MIC ». pour déterminer l’identificateur de chaîne pour une entrée donnée, utilisez les fonctions multimédias Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))et [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). pour plus d’informations, consultez la rubrique MSDN [Mixer les requêtes d’appareil](/windows/desktop/Multimedia/mixer-device-queries) .

Ajout du multiplexeur et du writer de fichier

Un graphique de capture audio doit contenir un multiplexeur et un writer de fichier.

Un *multiplexeur* est un filtre qui associe un ou plusieurs flux en un seul flux avec un format particulier. Par exemple, le filtre multiplexeur AVI combine des flux audio et vidéo dans un flux AVI entrelacé. Pour la capture audio, il n’y a généralement qu’un seul flux audio, mais les données audio doivent toujours être empaquetées dans un format qui peut être enregistré sur le disque, ce qui nécessite un multiplexeur. Le choix du multiplexeur dépend du format cible :

-   AVI : multiplexeur AVI
-   WAV : WavDest
-   WMA : enregistreur ASF

Un *enregistreur de fichier* est un filtre qui écrit des données entrantes dans un fichier. Pour les fichiers AVI ou WAV, utilisez le [filtre du writer de fichier](file-writer-filter.md). Pour les fichiers WMA, le writer ASF agit à la fois en tant que multiplexeur et writer de fichier.

Après avoir créé les filtres et les avoir ajoutés au graphique, connectez la broche de sortie du filtre de capture audio à la broche d’entrée du multiplexeur et connectez la broche de sortie du multiplexeur à la broche d’entrée du générateur de filtre (en supposant que ces filtres soient distincts). Pour spécifier le nom de fichier, interrogez le writer de fichier de l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) et appelez la méthode [**IFileSinkFilter :: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .

### <a name="example-code"></a>Exemple de code

L’exemple suivant montre comment générer un graphique de capture audio à l’aide du filtre WavDest. Les mêmes principes s’appliquent aux autres types de fichiers.


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



cet exemple utilise la `AddFilterByCLSID` fonction décrite dans [ajouter un filtre par CLSID](add-a-filter-by-clsid.md)et la `ConnectFilters` fonction décrite dans [Connecter deux filtres](connect-two-filters.md). aucun de ces deux n’est une API DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Capture audio](audio-capture.md)
</dt> </dl>

 

 
