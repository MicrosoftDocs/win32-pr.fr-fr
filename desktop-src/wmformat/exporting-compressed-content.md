---
title: Exportation du contenu compressé
description: Exportation du contenu compressé
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media Format SDK, exportation DRM
- Windows Media Format SDK, exporter
- Windows Media Format SDK, contenu compressé
- gestion des droits numériques (DRM), exportation
- DRM (gestion des droits numériques), exportation
- gestion des droits numériques (DRM), contenu compressé
- DRM (gestion des droits numériques), contenu compressé
- API étendues du client DRM, contenu compressé
- API étendues du client, contenu compressé
- API étendues du client DRM, exporter
- API étendues clientes, exporter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839802"
---
# <a name="exporting-compressed-content"></a>Exportation du contenu compressé

Cette section décrit l’exportation de médias protégés par DRM Windows Media sur un fichier Windows Media où l’application reçoit des données multimédias numériques compressées. Pour ce faire, votre application doit effectuer un déchiffrement en ligne de toutes les charges utiles chiffrées DRM Windows Media dans un fichier ASF.

> [!Note]  
> Une bibliothèque d’analyse ASF vous est fournie dans le cadre de l’accord d’exportation DRM Windows Media.

 

Les principales étapes impliquées dans l’exportation de contenu compressé sont les suivantes :

1.  Effectuez l’individualisation DRM, si nécessaire.
2.  Vérifiez que le schéma de protection de contenu cible est explicitement autorisé.
3.  Créez un objet déchiffreur pour déchiffrer chaque charge utile ASF.
4.  Le système DRM transforme chaque charge utile ASF de Windows Media DRM en RC4 avant de la transmettre à votre application.

Si votre application modifie la taille d’une charge utile ASF pendant la transchiffrement, vous devez également Remultiplexer le fichier ASF.

Transmettez à la bibliothèque stub un certificat d’application Windows Media DRM export. Le certificat est vérifié et, s’il est valide, le système DRM génère un vecteur d’initialisation et le chiffre à l’aide de RSA OAEP.

-   Une clé de session RC4 est créée pour chaque charge utile en concaténant le vecteur d’initialisation et une valeur salt. Vous fournissez la valeur Salt à l’API de déchiffrement, et vous devez l’incrémenter par une valeur entière positive différente de zéro pour chaque charge utile.

Microsoft vous fournira un outil de Microsoft dans le cadre de l’accord d’exportation Windows Media DRM qui vous permettra de générer votre propre paire de clés publique/privée RSA. Vous allez envoyer la clé publique à Microsoft, où Microsoft l’intégrera dans un certificat d’application DRM Windows Media signé et la renverra.

Chaque charge utile, une fois déchiffrée à l’aide de la clé de déchiffrement RC4, doit être immédiatement chiffrée dans le CPS de sortie. D’autres restrictions s’appliquent à la gestion des charges utiles non chiffrées qui sont décrites dans les règles de robustesse et de conformité, qui accompagnent le contrat d’exportation DRM Windows Media.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Déchiffrement et rechiffrement de la charge utile ASF**](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[**Exportation DRM**](drm-export.md)
</dt> <dt>

[**Réalisation de l’individualisation DRM**](performing-drm-individualization.md)
</dt> <dt>

[**Vérification et initialisation**](verification-and-initialization.md)
</dt> </dl>

 

 




