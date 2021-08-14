---
title: Insertion de formats de flux natifs dans des fichiers ASF (QASF)
description: Insertion de formats de flux natifs dans des fichiers ASF (QASF)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media Format SDK, Native Stream formats (QASF)
- Windows Media Format SDK, insertion de formats de flux natifs dans des fichiers ASF (QASF)
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), insertion de formats de flux natifs (QASF)
- ASF (format des systèmes avancés), insérer des formats de flux natifs (QASF)
- ASF (Advanced Systems Format), formats de flux natifs (QASF)
- ASF (format des systèmes avancés), formats de flux natifs (QASF)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, formats de flux natifs (QASF)
- DirectShow, insertion de formats de flux natifs dans des fichiers ASF (QASF)
- Windows Media Format SDK, QASF
- ASF (Advanced Systems Format), QASF
- ASF (format avancé des systèmes), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b395748520943a62645a88c018131f909577191ebafbe1f9c4d3a80219cb39f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701776"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a>Insertion de formats de flux natifs dans des fichiers ASF (QASF)

par défaut, l' [enregistreur ASF WM](wm-asf-writer-filter.md) attend des flux audio et vidéo non compressés sur ses broches d’entrée, et il utilise le kit de développement logiciel (SDK) de Format multimédia Windows pour accéder aux codecs de Windows Media Audio et de Windows Media Video, qui compressent les flux. Toutefois, le conteneur de fichiers ASF peut être utilisé pour n’importe quel type de données. En plaçant des données multimédias numériques dans un conteneur de fichiers ASF, vous pouvez ajouter des fonctionnalités fournies par ASF, telles que les métadonnées et la gestion des droits numériques (DRM), sans avoir à transcoder votre contenu.

pour créer un fichier ASF qui contient du contenu qui n’est pas Windows support, l’application doit compresser le flux dans le graphique de filtre en amont de l’enregistreur asf de wm et contourner le mécanisme de compression du writer asf en appelant [**IConfigAsfWriter2 :: SetParam**](iconfigasfwriter2-setparam.md) , comme suit :


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



Configurez ensuite le filtre avec le profil souhaité. Il est essentiel que le type de média du flux d’entrée corresponde exactement au format du profil. Dans certains cas, il peut être nécessaire d’examiner le format du flux d’entrée et de créer un profil personnalisé pour le faire correspondre. Pour plus d’informations, consultez [pour créer des fichiers ASF à l’aide de codecs tiers](to-create-asf-files-using-third-party-codecs.md).

Quand vous connectez l’enregistreur ASF WM au filtre amont, utilisez la méthode **IGraphBuilder :: ConnectDirect** . n’utilisez pas de méthodes de « connexion intelligente » comme **IGraphBuilder :: Connecter** ou **IGraphBuilder :: RenderFile** pour connecter le filtre, car cette opération désactive le mode « contournement de la compression » du filtre.

 

 




