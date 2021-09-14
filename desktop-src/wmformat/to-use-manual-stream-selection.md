---
title: Pour utiliser la sélection manuelle de flux
description: Pour utiliser la sélection manuelle de flux
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- ASF (Advanced Systems Format), sélection manuelle des flux
- ASF (format des systèmes avancés), sélection manuelle des flux
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), sélection de flux
- ASF (format de systèmes avancés), sélection de flux
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- lecteurs asynchrones, sélection manuelle de flux
- lecteurs asynchrones, sélection de flux
- flux, sélection manuelle
- exclusion mutuelle, sélection de flux manuelle
- flux, lecteurs asynchrones
- exclusion mutuelle, lecteurs asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225833"
---
# <a name="to-use-manual-stream-selection"></a>Pour utiliser la sélection manuelle de flux

Lorsque vous fournissez des exemples non compressés avec l’objet Reader, vous pouvez les remettre uniquement par numéro de sortie. Dans le cas de flux mutuellement exclusifs, cela signifie que vous ne pouvez recevoir des exemples qu’à partir d’un flux de l’exclusion mutuelle à la fois. Le processus qui consiste à choisir le flux mutuellement exclusif à remettre est appelé « sélection de flux ».

Pour l’exclusion mutuelle de la vitesse de transmission, le lecteur effectue automatiquement des sélections de flux en fonction des conditions sur l’ordinateur hôte lors de la lecture. Pour les autres types d’exclusion mutuelle, le lecteur fournit des exemples à partir du flux par défaut, sauf si vous sélectionnez manuellement un autre flux. Il peut également y avoir des instances lorsque vous souhaitez sélectionner un flux manuellement à partir d’une exclusion mutuelle à vitesse de transmission.

La sélection manuelle des flux est activée ou désactivée pour l’ensemble du fichier. Si un fichier contient une exclusion mutuelle à vitesse de transmission et d’autres types d’exclusion mutuelle, vous devez sélectionner manuellement les flux basés sur la vitesse de transmission.

Pour sélectionner manuellement un flux qui s’exclue mutuellement, vous devez effectuer les étapes suivantes.

1.  Récupérez un pointeur vers l’interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) de l’objet lecteur en appelant **IWMReader :: QueryInterface**.
2.  Activez la sélection manuelle des flux en appelant [**IWMReaderAdvanced :: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Pour déterminer si un flux particulier est sélectionné, appelez [**IWMReaderAdvanced :: GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). Vous devez passer un pointeur vers une variable du type d’énumération de la [**\_ \_ sélection de flux WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) . Lorsque l’appel est retourné, la valeur dans la variable décrit le type de sélection actuel du flux.
4.  Pour sélectionner un flux, appelez [**IWMReaderAdvanced :: SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Cette méthode vous permet de spécifier plusieurs flux en même temps pour le basculement de flux synchronisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur asynchrone**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




