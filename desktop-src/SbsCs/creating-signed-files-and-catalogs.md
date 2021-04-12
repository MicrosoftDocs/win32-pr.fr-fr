---
description: Pour signer un fichier et créer un catalogue pour celui-ci, vous devez d’abord disposer d’un processus de signature des fichiers, d’un certificat et d’une clé publique.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Création de fichiers et de catalogues signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203182"
---
# <a name="creating-signed-files-and-catalogs"></a>Création de fichiers et de catalogues signés

Pour signer un fichier et créer un catalogue pour celui-ci, vous devez d’abord disposer d’un processus de signature des fichiers, d’un certificat et d’une clé publique.

**Pour signer un fichier et créer un catalogue**

1.  Utilisez [Pktextract.exe](pktextract-exe.md) pour extraire le [*jeton de clé publique*](p-sbscs-gly.md) du fichier de certificat. Le fichier de certificat doit être présent dans le même répertoire que l’utilitaire.
2.  Utilisez la valeur de jeton de clé publique pour mettre à jour l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** dans le fichier manifeste.
3.  Utilisez [MT.exe](mt-exe.md) pour générer des hachages de fichiers contenus dans le manifeste de l’assembly et pour créer le fichier de description du catalogue (. CDF).
4.  Utilisez Makecat.exe avec le. CDF généré pour créer le catalogue de sécurité pour l’assembly. Cet outil est inclus dans l’CryptoAPI.
5.  Utilisez l’utilitaire [SignTool](/windows/desktop/SecCrypto/signtool) pour signer le catalogue généré avec le certificat utilisé à l’étape 1. Les étapes 3 et 4 du. CDF peuvent être supprimées une fois le catalogue créé.

Voir aussi [exemple de signature d’assembly](assembly-signing-example.md).

 

 
