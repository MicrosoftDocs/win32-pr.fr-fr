---
title: Pour configurer l’indexeur
description: Pour configurer l’indexeur
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK, configuration d’indexeurs
- ASF (Advanced Systems Format), configuration des indexeurs
- ASF (format des systèmes avancés), configuration des indexeurs
- index, configuration d’indexeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381537"
---
# <a name="to-configure-the-indexer"></a>Pour configurer l’indexeur

Vous pouvez configurer l’indexeur avant de l’utiliser pour indexer un fichier ASF. Chaque flux du fichier peut être configuré séparément, ou vous pouvez définir la même configuration pour tous les flux.

Si vous configurez plusieurs vapeurs pour l’indexation dans un fichier, vous devez les configurer toutes, puis commencer l’indexation. Si vous configurez et indexez un flux, puis configurez un autre flux dans le même fichier, le redémarrage de l’indexeur supprimera le premier index. Cela est conforme au format de fichier ASF.

Le code suivant montre comment configurer l’indexeur. Le code suppose que le fichier à indexer a deux flux : le premier est un flux audio qui n’a pas besoin d’être indexé et le second est un flux vidéo. Ce code illustre uniquement la configuration de l’indexeur. Pour indexer un fichier, vous devez suivre les étapes présentées dans [pour indexer un fichier ASF](to-index-an-asf-file.md).


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> Le type d’index par défaut est le \_ \_ point de nettoyage le plus proche de WMT \_ \_ . Bien que vous puissiez définir le type d’index sur d’autres valeurs, cela dégradera les performances de recherche.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMIndexer2 :: configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Pour indexer un fichier ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




