---
title: Entrée de registre des autorisations
description: Entrée de registre des autorisations
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, autorisations
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, autorisations
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- autorisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030780"
---
# <a name="permissions-registry-entry"></a>Entrée de registre des autorisations

Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension. La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md). L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée d' **autorisations** .

L’entrée **autorisations** spécifie les actions que le lecteur Windows Media est autorisé à effectuer sur les fichiers qui ont l’extension personnalisée. L’entrée d' **autorisation** se présente sous la forme suivante.



| Nom        | Type           | Valeur                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Autorisations | **\_valeur DWORD reg** | Ensemble d’indicateurs, chacun d’entre eux octroyant l’autorisation pour une action spécifique. |



 

La valeur de l’entrée d' **autorisation** est une **opération de bits or d'** un ou plusieurs des indicateurs suivants.



| Flag (valeur décimale) | Description                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Autorisation de lecture. Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être lus.                                                                                                                                                                                       |
| 2                    | Autorisation pour la suppression du dossier. Les fichiers dont l’extension de nom de fichier est enregistrée seront inclus dans la sélection créée lorsque l’utilisateur fait glisser un dossier contenant les fichiers et le supprime de l’interface utilisateur du lecteur.                                                      |
| 4                    | Autorisation pour CD multimédia. Les fichiers dont l’extension de nom de fichier est enregistrée seront inclus dans la sélection créée lorsqu’un CD contenant les fichiers est inséré dans le lecteur de CD-ROM.                                                                                           |
| 8                    | Autorisation pour la bibliothèque. Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être ajoutés à la bibliothèque. Requis pour les plug-ins de conversion.                                                                                                                                    |
| 16                   | Autorisation pour la diffusion en continu HTML. Les fichiers dont l’extension de nom de fichier est enregistrée sont insérés dans le cache Internet Explorer lorsqu’ils sont remis à partir d’un flux Web.                                                                                                            |
| 128                  | Autorisation de transcodage. Les fichiers dont l’extension de nom de fichier est enregistrée peuvent être transcodés au format Windows Media sous certaines conditions. Consultez [IWMPTranscodePolicy :: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Requiert le lecteur Windows Media 10 ou une version ultérieure. |



 

Lorsque l’utilisateur tente de lire un fichier multimédia qui a une extension de nom de fichier personnalisée, le lecteur Windows Media recherche une sous-clé de Registre qui correspond à l’extension. Si aucune correspondance n’est trouvée, le lecteur présente à l’utilisateur une boîte de dialogue d’avertissement qui demande à l’utilisateur l’autorisation d’essayer de lire le fichier. Si vous créez des fichiers multimédias numériques avec des extensions de nom de fichier personnalisées, vous pouvez empêcher l’affichage de cet avertissement sur l’ordinateur de l’utilisateur en inscrivant l’extension de nom de fichier et en fournissant une entrée d' **autorisation** .

L’entrée d' **autorisation** (à l’exception de la valeur d’indicateur 128) est prise en charge par le lecteur Windows Media 9 et versions ultérieures. La valeur d’indicateur 128 est prise en charge par le lecteur Windows Media 10 et versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




