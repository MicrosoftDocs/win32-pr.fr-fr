---
description: Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534183"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?

Il existe de nombreuses raisons pour lesquelles un décodeur peut rejeter un format. Les données de format étendu sont manquantes ou incorrectes. Les données de format étendu sont des informations spécifiques au codec qui sont ajoutées à la structure décrivant le type de média.

Quand vous énumérez un type de sortie à l’aide d’un objet encodeur, le membre **pbFormat** de la structure de  [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) pointera vers une structure WAVEFORMATEX. Les données de format étendu sont ajoutées à cette structure et la taille de ces données est stockée dans le membre **WAVEFORMATEX. cbSize** . Quel que soit le conteneur utilisé pour stocker les données compressées, vous devez conserver la structure **WAVEFORMATEX** et l’utiliser dans le type d’entrée pour le décodeur. Sans les données de format étendu, le décodeur ne peut pas décompresser le contenu.

Pour les formats vidéo, vous devez récupérer manuellement les données de format étendu et les ajouter à la structure **VIDEOINFOHEADER** . Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Questions fréquentes (FAQ)](frequentlyaskedquestions.md)
</dt> </dl>

 

 
