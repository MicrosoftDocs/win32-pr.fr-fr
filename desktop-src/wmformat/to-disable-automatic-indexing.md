---
title: Pour désactiver l’indexation automatique
description: Pour désactiver l’indexation automatique
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media Format SDK, désactivation de l’indexation automatique
- Windows Media Format SDK, indexation automatique
- ASF (Advanced Systems Format), désactivation de l’indexation automatique
- ASF (format de systèmes avancés), désactivation de l’indexation automatique
- ASF (Advanced Systems Format), indexation automatique
- ASF (format de systèmes avancés), indexation automatique
- index, désactivation de l’indexation automatique
- index, indexation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0235ddac8093d9b1c6d40fde341ee32d078b84b7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940691"
---
# <a name="to-disable-automatic-indexing"></a>Pour désactiver l’indexation automatique

Il se peut que vous ne souhaitiez pas toujours qu’un index soit généré par défaut lors de l’écriture d’un fichier ASF. Vous pouvez désactiver l’indexation automatique à l’aide de la méthode [**IWMWriterFileSink3 :: SetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) .

L’exemple de code suivant montre comment désactiver l’indexation automatique par le writer.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




