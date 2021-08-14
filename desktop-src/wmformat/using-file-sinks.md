---
title: Utilisation de récepteurs de fichiers
description: Utilisation de récepteurs de fichiers
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), récepteurs de fichiers
- ASF (format des systèmes avancés), récepteurs de fichiers
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs de fichiers
- récepteurs de fichiers, à propos de
- récepteurs de fichiers, création
- récepteurs de fichiers, arrêt
- récepteurs de fichiers, démarrage
- récepteurs de fichiers, fermeture
- récepteurs, statistiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f94bd6698ca30a645957da36cf3b81a84f9d3e7c8ce6c598be2c39f8ac766db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196172"
---
# <a name="using-file-sinks"></a>Utilisation de récepteurs de fichiers

Dans des circonstances normales, vous pouvez simplement transmettre à l’enregistreur un nom de fichier de sortie à l’aide de la méthode [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , et l’objet enregistreur écrira automatiquement le fichier sur le disque. Dans ce cas, l’enregistreur crée et contrôle un objet récepteur de fichiers de writer qui gère l’écriture du fichier sur le disque. Un objet récepteur de fichiers du writer contrôle le déroulement des données de l’objet Writer dans un fichier unique.

Vous pouvez créer vos propres récepteurs de fichiers pour mieux contrôler la façon dont le récepteur écrit le fichier. Vous pouvez également accéder au récepteur de fichiers du writer par défaut créé par le writer en réponse à un appel à **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Création de récepteurs de fichiers

Pour créer un récepteur de fichiers et l’ajouter au writer, procédez comme suit.

1.  Créez un récepteur en appelant la fonction [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .
2.  Fournissez un nom de fichier pour le récepteur en appelant [**IWMWriterFileSink :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Ajoutez le récepteur de fichiers au writer en appelant [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Effectuez l’écriture de la manière habituelle.
5.  Une fois l’écriture terminée, le récepteur ferme automatiquement le fichier.

## <a name="stopping-and-starting-file-sinks"></a>Arrêt et démarrage des récepteurs de fichiers

Une fois les opérations d’écriture commencées, vous pouvez arrêter l’écriture dans un récepteur de fichiers en appelant [**IWMWriterFileSink2 :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Il existe de nombreuses raisons possibles pour lesquelles vous souhaiteriez arrêter l’écriture dans un récepteur. Par exemple, si vous enregistrez à partir d’une source active, vous pouvez être intéressé uniquement par une partie du contenu.

Vous pouvez reprendre l’écriture dans un récepteur de fichiers en appelant [**IWMWriterFileSink2 :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Les deux options **arrêter** et **Démarrer** utilisent des durées de présentation pour contrôler approximativement le moment où la commande est exécutée. Vous pouvez utiliser les méthodes [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) pour mieux contrôler les heures de démarrage et d’arrêt.

## <a name="closing-file-sinks"></a>Fermeture des récepteurs de fichiers

Normalement, un récepteur de fichiers est fermé automatiquement. Si vous avez terminé l’écriture dans un récepteur, mais que l’écriture d’opérations sur d’autres récepteurs se poursuit, vous devez fermer explicitement le récepteur pour conserver les ressources. Pour fermer un récepteur de fichiers, appelez [**IWMWriterFileSink2 :: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Obtention des statistiques du récepteur

Vous pouvez obtenir la taille de fichier et la durée d’un récepteur ouvert en appelant [**IWMWriterFileSink2 :: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) et [**IWMWriterFileSink2 :: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectivement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**Interface IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**Interface IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Récepteur de fichiers d’auteur, objet**](writer-file-sink-object.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




