---
title: Pour créer un lecteur synchrone et ouvrir un fichier
description: Pour créer un lecteur synchrone et ouvrir un fichier
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), création de lecteurs
- ASF (format avancé des systèmes), création de lecteurs
- ASF (Advanced Systems Format), ouvrir des fichiers
- ASF (format des systèmes avancés), ouvrir des fichiers
- lecteurs synchrones, création
- lecteurs synchrones, ouverture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106509839"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Pour créer un lecteur synchrone et ouvrir un fichier

Avant de pouvoir travailler avec le lecteur synchrone, vous devez créer un objet lecteur synchrone et charger un fichier en lecture. Pour initialiser le lecteur synchrone et ouvrir un fichier, procédez comme suit.

1.  Créez un objet lecteur synchrone en appelant la fonction [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) . Vous devez spécifier le niveau de gestion des droits souhaité pour le nouvel objet lecteur. Les modes disponibles sont répertoriés dans le type d’énumération des **\_ droits WMT** .
2.  Spécifiez un fichier à lire en appelant [**IWMSyncReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

Le lecteur synchrone prend également en charge l’utilisation de l’interface com **IStream** pour ouvrir des fichiers. Vous pouvez implémenter l’interface **IStream** comme vous le souhaitez. Une fois le fichier souhaité ouvert dans **IStream**, vous pouvez suivre les étapes décrites ci-dessus, sauf que vous devez appeler [**IWMSyncReader :: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) au lieu de **IWMSyncReader :: Open** à l’étape 2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




