---
title: Écriture d’exemples compressés
description: Écriture d’exemples compressés
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- ASF (Advanced Systems Format), écrire des exemples compressés
- ASF (format avancé des systèmes), écriture d’exemples compressés
- ASF (Advanced Systems Format), passer des exemples compressés
- ASF (format de systèmes avancés), passer des exemples compressés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195852"
---
# <a name="writing-compressed-samples"></a>Écriture d’exemples compressés

Pour certains flux audio ou vidéo, vous souhaiterez peut-être passer des exemples qui sont déjà compressés au lieu de transmettre des données brutes. Cette fonctionnalité permet de copier un flux existant ou d’écrire des exemples compressés à l’aide d’un codec tiers. Le processus d’écriture d’un exemple compressé est identique à l’écriture d’un exemple non compressé, sauf que vous utilisez [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) au lieu de [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Pour plus d’informations sur l’écriture d’exemples non compressés, consultez [pour écrire des exemples](to-write-samples.md).

Lorsque vous écrivez des exemples compressés, pour les profils CBR, le writer supprime certains exemples, si nécessaire, pour conserver le contenu dans les valeurs de la vitesse de transmission et de la fenêtre tampon spécifiées. Pour VBR, l’enregistreur ne supprimera pas les exemples, mais il n’existe aucun moyen de s’assurer que les valeurs de la vitesse de transmission et de la fenêtre de mémoire tampon seront correctes.

Si vous copiez un flux d’un fichier vers un autre, vous devez toujours copier l’objet de configuration de flux à partir du profil du fichier d’origine vers le profil du nouveau fichier. Cela garantit que vous disposez des informations de vitesse de transmission et de fenêtre de mémoire tampon appropriées. Si vous copiez un flux compressé dans un flux qui a une fenêtre de mémoire tampon inférieure définie, des exemples seront supprimés lors de l’écriture du fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




