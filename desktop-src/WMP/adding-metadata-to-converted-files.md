---
title: Ajout de métadonnées aux fichiers convertis
description: Ajout de métadonnées aux fichiers convertis
ms.assetid: 97588651-23de-43ab-b884-76d8af95ab93
keywords:
- Windows Media Player, processus de conversion
- Plug-ins du lecteur Windows Media, conversion
- plug-ins, conversion
- plug-ins de conversion, ajout de métadonnées aux fichiers convertis
- ajout de métadonnées aux fichiers convertis
- métadonnées, ajouter aux fichiers convertis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4ae47318089149564f64832c95e4cee1b27f26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727733"
---
# <a name="adding-metadata-to-converted-files"></a>Ajout de métadonnées aux fichiers convertis

Les fichiers convertis doivent contenir certaines métadonnées pour garantir une expérience utilisateur optimale. Au minimum, les fichiers convertis doivent contenir les attributs principaux figurant dans les [instructions d’utilisation des métadonnées Windows Media](/previous-versions/ms867702(v=msdn.10)).

Pour les fichiers musicaux, définissez la valeur de **WM/MediaClassPrimaryID** sur D1607DBC-E323-4BE2-86A1-48A42A28441E.

Pour les fichiers de messagerie vocale, définissez la valeur de **WM/MediaClassPrimaryID** sur 01CD0F29-DA4E-4157-897b-6275D50C4F11, qui est le GUID de la classe principale pour les fichiers audio. Définissez la valeur de **WM/MediaClassSecondaryID** sur 193c8824-4D52-4178-90BD-305240b04636.

Pour les notes vocales, définissez la valeur de **WM/MediaClassPrimaryID** sur 01CD0F29-DA4E-4157-897b-6275D50C4F11. Définissez la valeur de **WM/MediaClassSecondaryID** sur 3A172A13-2BD9-4831-835B-114F6A95943F.

Définissez la valeur de **WM/ContentDistributor** sur le nom de clé du service musical qui a fourni le contenu.

Définissez la valeur de **WM/UniqueFileIdentifier** sur l’ID de contenu. Cela vous permettra de récupérer des éléments de contenu spécifiques à un moment ultérieur.

Définissez une valeur pour **WM/WMShadowFileSourceFileType**.

Pour le contenu protégé, utilisez le kit de développement logiciel (SDK) Windows Media format pour définir l’attribut **DRM \_ DRMHeader \_ CONTENTID** sur l’ID de contenu.

Pour le contenu protégé, définissez une valeur pour **WM/WMShadowFileSourceDRMType**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des plug-ins de conversion**](about-conversion-plug-ins.md)
</dt> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 