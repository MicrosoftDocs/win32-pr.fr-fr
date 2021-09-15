---
title: Fonctionnalités du codec
description: Fonctionnalités du codec
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- Windows Media Format SDK, fonctionnalités de codec
- Windows Media Format SDK, fonctionnalités
- codecs, fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294475"
---
# <a name="codec-features"></a>Fonctionnalités du codec

le kit de développement logiciel (SDK) Windows Media Format est fourni avec plusieurs codecs audio et vidéo. Vous pouvez utiliser les codecs fournis pour compresser et décompresser du contenu pour répondre à différents besoins. Le codec utilisé par le writer pour compresser les données est spécifié par les informations de configuration de flux dans le profil. Les informations du profil sont ensuite stockées dans l’en-tête du fichier créé par le writer. Ensuite, lorsque le fichier est ouvert par le lecteur ou le lecteur synchrone, les informations de profil dans l’en-tête identifient le codec nécessaire pour décompresser les données.

Les fonctionnalités suivantes sont présentées dans cette section.

-   [Codecs pris en charge](supported-codecs.md)
-   [Encodage à débit binaire constant (CBR)](constant-bit-rate--cbr--encoding.md)
-   [Encodage à vitesse de transmission variable (VBR)](variable-bit-rate--vbr--encoding.md)
-   [Encodage en deux passes](two-pass-encoding.md)
-   [Prise en charge audio haute résolution](high-resolution-audio-support.md)
-   [Audio à faible retards](low-delay-audio.md)
-   [Sortie audio S/PDIF](s-pdif-audio-output.md)
-   [Image vidéo](video-image.md)
-   [Modèles de conformité des appareils](device-conformance-templates.md)
-   [Paramètres de la complexité de la vidéo](video-complexity-settings.md)
-   [Interpolation de frame](frame-interpolation.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités**](features.md)
</dt> </dl>

 

 




