---
title: Déchiffrement et rechiffrement de la charge utile ASF
description: Déchiffrement et rechiffrement de la charge utile ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows Media Format SDK, ASF de déchiffrement et de chiffrement de la charge utile
- Windows Media Format SDK, déchiffrement de la charge utile et rechiffrement
- Windows Media Format SDK, déchiffrement
- Windows Media Format SDK, rechiffrement
- gestion des droits numériques (DRM), déchiffrement et rechiffrement de la charge utile ASF
- DRM (gestion des droits numériques), déchiffrement et rechiffrement de la charge utile ASF
- gestion des droits numériques (DRM), déchiffrement et rechiffrement de la charge utile
- DRM (gestion des droits numériques), déchiffrement et rechiffrement de la charge utile
- gestion des droits numériques (DRM), déchiffrement
- DRM (gestion des droits numériques), déchiffrement
- gestion des droits numériques (DRM), rechiffrement
- DRM (gestion des droits numériques), rechiffrement
- API étendues du client DRM, déchiffrement de la charge utile ASF et rechiffrement
- API étendues clientes, déchiffrement et rechiffrement de la charge utile ASF
- API étendues du client DRM, déchiffrement de la charge utile et rechiffrement
- API étendues clientes, déchiffrement de la charge utile et rechiffrement
- API étendues du client DRM, déchiffrement
- API étendues clientes, déchiffrement
- API étendues du client DRM, rechiffrement
- API étendues du client, rechiffrement
- ASF (Advanced Systems Format), rechiffrement
- ASF (format des systèmes avancés), rechiffrement
- ASF (Advanced Systems Format), déchiffrement
- ASF (format de systèmes avancés), déchiffrement
- ASF (Advanced Systems Format), déchiffrement et rechiffrement de la charge utile
- ASF (format avancé des systèmes), déchiffrement et rechiffrement de la charge utile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c60469ff0b1408fcf51cb3dde899559980790a09c01b6619b3ff2ba797554a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007109"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Déchiffrement et rechiffrement de la charge utile ASF

Les étapes ci-dessous décrivent les actions qu’une application doit effectuer pour déchiffrer et rechiffrer chaque charge utile :

1.  Incrémentez la valeur salt.
2.  transmettez la charge utile (chiffrée avec Windows Media DRM) et la valeur salt à la fonction de déchiffrement, [**IWMDRMDecrypt ::D ecrypt**](iwmdrmdecrypt-decrypt.md), qui renverra la charge utile, chiffrée à l’aide de la clé publique RC4.
3.  Dérivez une clé de transitive RC4 en appliquant un hachage SHA-1 du vecteur d’initialisation concaténé avec la valeur salt.
4.  Utilisez votre clé transitoire pour déchiffrer la charge utile.
5.  rechiffrez immédiatement la charge utile avec le schéma de protection de contenu autorisé, conformément aux règles de conformité et de robustesse de l’exportation DRM de Windows.
6.  Recherchez la charge utile suivante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exportation du contenu compressé**](exporting-compressed-content.md)
</dt> </dl>

 

 




