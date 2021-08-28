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
ms.openlocfilehash: 20e7e8e6d71e4104d65336b131d0e15d5eaedd8b2fba4b7715f5e60aa6083544
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055499"
---
# <a name="exporting-compressed-content"></a>Exportation du contenu compressé

cette section décrit l’exportation Windows média protégé par DRM sur un fichier multimédia Windows où l’application reçoit des données multimédias numériques compressées. pour ce faire, votre application doit effectuer un déchiffrement en ligne de toutes les charges utiles chiffrées DRM Windows dans un fichier ASF.

> [!Note]  
> une bibliothèque d’analyse ASF vous est fournie dans le cadre de l’accord d’exportation DRM Windows.

 

Les principales étapes impliquées dans l’exportation de contenu compressé sont les suivantes :

1.  Effectuez l’individualisation DRM, si nécessaire.
2.  Vérifiez que le schéma de protection de contenu cible est explicitement autorisé.
3.  Créez un objet déchiffreur pour déchiffrer chaque charge utile ASF.
4.  le système drm transforme chaque charge utile ASF à partir d’Windows Media drm en RC4 avant de la transmettre à votre application.

Si votre application modifie la taille d’une charge utile ASF pendant la transchiffrement, vous devez également Remultiplexer le fichier ASF.

transmettez à la bibliothèque stub un certificat d’Application d’exportation DRM Windows Media. Le certificat est vérifié et, s’il est valide, le système DRM génère un vecteur d’initialisation et le chiffre à l’aide de RSA OAEP.

-   Une clé de session RC4 est créée pour chaque charge utile en concaténant le vecteur d’initialisation et une valeur salt. Vous fournissez la valeur Salt à l’API de déchiffrement, et vous devez l’incrémenter par une valeur entière positive différente de zéro pour chaque charge utile.

Microsoft vous fournira un outil par Microsoft dans le cadre de l’accord d’exportation DRM Windows qui vous permettra de générer votre propre paire de clés publique/privée RSA. vous allez envoyer la clé publique à microsoft, où microsoft l’intégrera dans un certificat d’Application DRM Windows signé et la renverra.

Chaque charge utile, une fois déchiffrée à l’aide de la clé de déchiffrement RC4, doit être immédiatement chiffrée dans le CPS de sortie. d’autres restrictions s’appliquent à la gestion des charges utiles non chiffrées, qui sont décrites dans les règles de robustesse et de conformité, qui accompagnent le contrat d’exportation DRM Windows Media.

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

 

 




