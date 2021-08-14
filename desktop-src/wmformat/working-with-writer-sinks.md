---
title: Utilisation des récepteurs d’écriture
description: Utilisation des récepteurs d’écriture
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), récepteurs d’écriture
- ASF (format de systèmes avancés), récepteurs d’écriture
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs d’écriture
- récepteurs d’écriture, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407e5bf2e87bfbf3084d19f75170a12be693d804d4d902f919096dca5aeab057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194866"
---
# <a name="working-with-writer-sinks"></a>Utilisation des récepteurs d’écriture

l’objet writer de Windows media Format SDK traite les données de média d’entrée dans un flux de bits. Toutefois, l’objet Writer ne remet pas le flux binaire à sa destination finale (dans un fichier ou un emplacement réseau). Pour écrire le contenu ASF dans un format utilisable, vous devez utiliser des récepteurs d’enregistreur.

L’objet Writer prend en charge trois types de récepteurs : les récepteurs de fichiers, les récepteurs réseau et les récepteurs push. Un récepteur de fichiers écrit du contenu ASF dans un fichier ASF sur le disque. Un récepteur réseau diffuse du contenu ASF à partir d’une adresse réseau. un récepteur de notifications push transmet des données à un serveur exécutant Services Windows Media afin que le serveur puisse mettre le contenu à la disposition du public visé. Vous pouvez également créer vos propres récepteurs pour fournir des données ASF de la manière requise par votre application. Pour plus d’informations sur les récepteurs réseau et les récepteurs de notifications push, consultez [envoi de données ASF sur un réseau](sending-asf-data-over-a-network.md). Le reste de cette section traite des récepteurs d’écriture.

Vous pouvez configurer un ou plusieurs récepteurs pour chaque instance du writer que vous utilisez. Chaque récepteur ne gère qu’une seule destination. Par exemple, si vous souhaitez écrire trois fichiers à la fois, vous devez créer et configurer un récepteur de fichiers distinct pour chacun d’entre eux.

Les sections suivantes décrivent l’utilisation des récepteurs de Writers.



| Section                                                                      | Description                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Ajout de récepteurs à l’enregistreur](adding-sinks-to-the-writer.md)                 | Décrit comment ajouter des récepteurs au writer.                                        |
| [Énumération des récepteurs](enumerating-sinks.md)                                   | Décrit comment énumérer les récepteurs qui ont été ajoutés au writer.         |
| [Obtention de messages d’erreur à partir d’un récepteur](getting-error-messages-from-a-sink.md) | Décrit comment configurer des récepteurs pour remettre des messages d’État à votre application. |
| [Utilisation de récepteurs de fichiers](using-file-sinks.md)                                     | Décrit comment utiliser un récepteur de fichiers de Writer pour créer un fichier ASF sur le disque.           |
| [Utilisation de récepteurs personnalisés](using-custom-sinks.md)                                 | Décrit comment créer et utiliser vos propres récepteurs personnalisés pour fournir des données ASF.       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Interface IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




