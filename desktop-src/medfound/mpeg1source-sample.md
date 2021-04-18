---
description: Exemple MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Exemple MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519790"
---
# <a name="mpeg1source-sample"></a>Exemple MPEG1Source

Montre comment écrire une source de média personnalisée dans Microsoft Media Foundation. L’exemple implémente une source de média qui analyse les flux de couche de systèmes MPEG-1 et génère des exemples qui contiennent des charges utiles MPEG-1.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Avant d’examiner cet exemple, vous souhaiterez peut-être examiner l' [exemple WavSource](wavsource-sample.md), qui fournit une implémentation plus simple d’une source de média. L’exemple MPEG1Source ajoute certaines fonctionnalités qui se trouvent dans la plupart des implémentations réelles d’une source de média :

-   Plusieurs flux de données
-   Méthodes asynchrones
-   E/s asynchrones

Dans l’SDK Windows pour Windows Server 2008, cet exemple comprend également un exemple de décodeur vidéo MPEG-1 qui affiche le code de temps de chaque image vidéo. (Il ne décode pas en fait le flux binaire MPEG-1.)

À partir de la SDK Windows pour Windows 7, le décodeur a été déplacé vers un exemple distinct. Consultez [exemple de décodeur](decoder-sample.md).

## <a name="usage"></a>Utilisation

L’exemple MPEG1Source génère une DLL qui est un serveur COM pour la source du média, le gestionnaire de flux d’octets de la source du média et la table MFT du décodeur. Avant d’utiliser la source du média, vous devez inscrire la DLL.

Pour utiliser la source du média, vous pouvez exécuter l' [exemple BasicPlayback](/previous-versions//bb970475(v=vs.85)). Le programme de résolution source chargera automatiquement la source du média si vous sélectionnez un fichier MPEG-1 pour la lecture. (Si une erreur se produit, assurez-vous que vous avez correctement inscrit la DLL MPEG1Source.)

Vous pouvez également utiliser l’outil TopoEdit pour générer une topologie de lecture qui contient la source du média. Pour plus d’informations sur TopoEdit, consultez [TopoEdit](topoedit.md).

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Gestionnaires de schémas et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Didacticiel : écriture d’une source de média personnalisée](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Exemple WavSource](wavsource-sample.md)
</dt> </dl>

 

 
