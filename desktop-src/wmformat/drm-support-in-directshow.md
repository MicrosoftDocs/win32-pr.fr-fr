---
title: Prise en charge de DRM dans DirectShow
description: Prise en charge de DRM dans DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, prise en charge de DRM dans DirectShow
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, gestion des droits numériques (DRM)
- ASF (Advanced Systems Format), prise en charge de DRM dans DirectShow
- ASF (Advanced Systems Format), prise en charge de DRM dans DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), gestion des droits numériques (DRM)
- ASF (format de systèmes avancés), gestion des droits numériques (DRM)
- DirectShow, prise en charge de DRM
- gestion des droits numériques (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195996"
---
# <a name="drm-support-in-directshow"></a>Prise en charge de DRM dans DirectShow

la lecture et l’écriture de fichiers protégés par DRM dans DirectShow s’effectuent de la même façon que lorsque vous utilisez directement le kit de développement logiciel (SDK) du Format Windows Media. Pour commencer, vous avez besoin de la bibliothèque statique wmstubdrm, qui est obtenue séparément de Microsoft. en outre, vous devez implémenter l’interface **IKeyProvider** pour permettre à votre application d’accéder aux objets d’exécution du kit de développement logiciel (SDK) du Format multimédia Windows lorsque la gestion DRM est activée.

Lors de l’application de la protection DRM version 1, utilisez l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , qui est obtenue comme décrit dans [lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md). Lors de l’application de la protection DRM version 7, obtenez l’interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) en appelant **QueryService** sur le filtre du [writer WM ASF](wm-asf-writer-filter.md) , comme indiqué dans l’extrait de code, plus loin dans cette rubrique.

Toutes les autres configurations spécifiques à DRM sont exactement les mêmes que celles décrites dans activation de la [prise en charge de DRM](enabling-drm-support.md). Utilisez **QueryService** pour obtenir l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) à partir du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) .

DirectX 9,0 contient un exemple, PlayWndASF, une application de lecteur DirectShow compatible drm qui illustre l’acquisition de licence drm version 1 et version 7. Cet exemple comprend également une implémentation de la classe **CKeyProvider** , qui prend en charge l’interface **IKeyProvider** .

 

 




