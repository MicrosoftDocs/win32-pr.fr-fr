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
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101257"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Pour récupérer des exemples compressés avec le lecteur synchrone

À l’instar du lecteur asynchrone, le lecteur synchrone peut également récupérer des exemples compressés. Les exemples compressés doivent être utilisés lors de la copie de flux d’un fichier vers un autre.

Le kit de développement logiciel (SDK) Windows Media format ne fournit aucune méthode pour décoder les données après leur extraction à partir d’un fichier ASF. Si vous recevez des exemples compressés et que vous souhaitez les décompresser ultérieurement, vous devrez fournir votre propre code pour ce faire. Une façon de contourner cette limitation consiste à écrire les exemples compressés dans un nouveau fichier ASF, puis à les relire dans des exemples normaux et non compressés.

Pour recevoir des exemples compressés avec le lecteur synchrone, appelez [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) avant ou pendant la lecture. Pass true pour *fCompressed*.

> [!Note]  
> Les flux d’images ne sont pas valides pour la remise du flux compressé. Si vous copiez un flux d’image d’un fichier vers un autre, il ne fonctionnera pas dans le nouveau fichier. Pour copier un flux d’image à partir d’un fichier vers un fichier, récupérez les exemples de flux d’image par numéro de sortie et incluez-les dans le nouveau fichier comme si vous incluiez un nouveau flux d’image.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




