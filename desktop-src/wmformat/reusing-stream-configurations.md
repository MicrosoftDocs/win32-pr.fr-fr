---
title: Réutilisation des configurations de flux
description: Réutilisation des configurations de flux
ms.assetid: e2263c3a-56cd-4505-acd7-510dc7bac166
keywords:
- flux, réutilisation des configurations
- profils, réutilisation des configurations de flux
- réutilisation des configurations de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af10fd026904ccef33aba28d28e0e6a4975d3fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106538992"
---
# <a name="reusing-stream-configurations"></a>Réutilisation des configurations de flux

Il arrive souvent que vous souhaitiez réutiliser un objet de configuration de flux à partir d’un profil existant. Vous pouvez avoir des anciens profils qui nécessitent une mise à jour ou vous pouvez avoir besoin d’un flux identique à celui d’un profil système. Il est plus facile de réutiliser des configurations de flux que d’en créer d’autres, et vous pouvez souvent modifier quelques paramètres dans une configuration pour répondre à vos besoins plutôt que d’en créer un entièrement nouveau.

N’oubliez pas qu’il existe des limitations quant à la façon dont vous pouvez modifier les configurations de flux. Si vous modifiez les paramètres de manière incorrecte, il se peut que votre profil n’accepte pas l’objet de configuration de flux. Les configurations de flux incorrectes sont souvent acceptées par le profil, mais provoquent le rejet du profil par l’objet enregistreur. Tenez compte des limitations et des problèmes suivants lors de l’utilisation et de la modification de configurations de flux existantes.

-   Ne modifiez jamais le contenu d’un fichier. prx pour modifier les paramètres de flux. Lorsque les profils sont enregistrés dans des chaînes XML et écrits dans un fichier. prx, ils peuvent être lus à l’aide de n’importe quel éditeur de texte. L’examen d’un profil enregistré peut vous aider à comprendre le fonctionnement des profils. Toutefois, vous ne devez jamais modifier un fichier. prx de quelque manière que ce soit. Même les modifications apparemment triviales peuvent invalider le profil.
-   Plusieurs versions du codec Windows Media Audio utilisent les mêmes configurations de flux. Si vous avez un objet de configuration de flux configuré en tant que sous-type WMMEDIASUBTYPE \_ WMAudioV2, WMMEDIASUBTYPE \_ WMAUDIOV7 ou WMMEDIASUBTYPE \_ WMAudioV8, le flux résultant sera compressé avec le dernier Windows Media Audio Codec. Toutefois, vous devez évaluer vos besoins avant d’utiliser un codec audio existant. De nombreux types de fichiers peuvent être améliorés en effectuant une mise à niveau vers la dernière version du codec Windows Media Audio Professional ou le codec Windows Media Audio Lossless.
-   Ne modifiez jamais le sous-type d’un flux pour le mettre à niveau vers un nouveau codec. Lorsque vous utilisez les méthodes de [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) pour obtenir une configuration de flux, le codec y attache des données qui identifient le format de flux binaire. Si vous modifiez le sous-type d’un objet de configuration de flux existant, le sous-type ne correspondra pas aux données du codec. Un profil avec une telle configuration de flux n’est pas accepté par l’objet Writer.
-   Ne modifiez pas les paramètres des configurations de flux audio compressé. Si les paramètres d’un flux audio ne répondent pas à vos besoins, obtenez une nouvelle configuration de flux à partir du codec à l’aide des méthodes de **IWMCodecInfo3**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de flux**](configuring-streams.md)
</dt> <dt>

[**Obtention d’informations de configuration de flux à partir de codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




