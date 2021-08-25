---
title: Pour récupérer des exemples compressés avec le lecteur synchrone
description: Pour récupérer des exemples compressés avec le lecteur synchrone
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- ASF (Advanced Systems Format), récupération des exemples compressés
- ASF (format des systèmes avancés), récupération des exemples compressés
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- ASF (Advanced Systems Format), exemples compressés
- ASF (Advanced Systems Format), exemples compressés
- lecteurs synchrones, récupération des exemples compressés
- lecteurs synchrones, exemples compressés
- exemples compressés, récupération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb2e3c7f1f6e00bd3f1c215a3b6783387fd3e19c268afe58862aa4b4d61889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807459"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Pour récupérer des exemples compressés avec le lecteur synchrone

À l’instar du lecteur asynchrone, le lecteur synchrone peut également récupérer des exemples compressés. Les exemples compressés doivent être utilisés lors de la copie de flux d’un fichier vers un autre.

le kit de développement logiciel (SDK) Windows Media Format ne fournit aucune méthode pour décoder les données après leur extraction à partir d’un fichier ASF. Si vous recevez des exemples compressés et que vous souhaitez les décompresser ultérieurement, vous devrez fournir votre propre code pour ce faire. Une façon de contourner cette limitation consiste à écrire les exemples compressés dans un nouveau fichier ASF, puis à les relire dans des exemples normaux et non compressés.

Pour recevoir des exemples compressés avec le lecteur synchrone, appelez [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) avant ou pendant la lecture. Pass true pour *fCompressed*.

> [!Note]  
> Les flux d’images ne sont pas valides pour la remise du flux compressé. Si vous copiez un flux d’image d’un fichier vers un autre, il ne fonctionnera pas dans le nouveau fichier. Pour copier un flux d’image à partir d’un fichier vers un fichier, récupérez les exemples de flux d’image par numéro de sortie et incluez-les dans le nouveau fichier comme si vous incluiez un nouveau flux d’image.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




