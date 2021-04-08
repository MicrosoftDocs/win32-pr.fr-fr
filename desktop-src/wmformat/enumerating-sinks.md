---
title: Énumération des récepteurs
description: Énumération des récepteurs
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), énumération des récepteurs
- ASF (format avancé des systèmes), énumération des récepteurs
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724031"
---
# <a name="enumerating-sinks"></a>Énumération des récepteurs

Plusieurs récepteurs peuvent être associés à l’enregistreur. Vous pouvez énumérer les récepteurs qui ont été ajoutés au writer à l’aide de [**IWMWriterAdvanced :: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) et [**IWMWriterAdvanced :: GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

L’exemple de code dans l' [obtention de messages d’erreur à partir d’un récepteur](getting-error-messages-from-a-sink.md) démontre l’énumération du récepteur.

> [!Note]  
> Lors de l’énumération des récepteurs, le récepteur de fichiers par défaut créé en réponse à un appel à [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) est énuméré avec tout autre récepteur que vous avez ajouté. Si vous utilisez uniquement le récepteur de fichiers par défaut, vous pouvez y accéder en appelant **GetSink** pour l’index de récepteur 0.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




