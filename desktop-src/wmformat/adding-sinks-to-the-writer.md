---
title: Ajout de récepteurs à l’enregistreur
description: Ajout de récepteurs à l’enregistreur
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- ASF (Advanced Systems Format), ajout de récepteurs à l’enregistreur
- ASF (format de systèmes avancés), ajout de récepteurs à l’enregistreur
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- ASF (Advanced Systems Format), récepteurs d’écriture
- ASF (format de systèmes avancés), récepteurs d’écriture
- récepteurs, ajout au writer
- récepteurs d’écriture, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381517"
---
# <a name="adding-sinks-to-the-writer"></a>Ajout de récepteurs à l’enregistreur

Les récepteurs d’écriture sont des objets distincts du writer et doivent être ajoutés au Writer pour être utilisés. Si vous écrivez dans un fichier, vous pouvez simplement appeler [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), ce qui permet de configurer automatiquement le récepteur de fichiers. Sinon, pour ajouter un récepteur au writer, appelez la méthode [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) . **AddSink** requiert un pointeur vers l’interface [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) du récepteur.

Lorsque vous avez terminé d’utiliser un récepteur, vous devez le fermer en appelant la méthode appropriée, en fonction du type de récepteur, puis le supprimer du writer en appelant [**IWMWriterAdvanced :: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

L’exemple de code suivant montre comment créer un récepteur de fichiers d’écriture et l’ajouter au writer. Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Obtention de messages d’erreur à partir d’un récepteur**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




