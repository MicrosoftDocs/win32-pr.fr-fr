---
description: Cette section détaille la version binaire du format de fichier DirectX (. x), telle qu’elle a été introduite dans la version de DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Encodage Binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f35d4ccd33692cc25c2b99c8c20ed53dc0c7a01a488c738992a9a4f22fbc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460758"
---
# <a name="binary-encoding"></a>Encodage Binaire

Cette section détaille la version binaire du format de fichier DirectX (. x), telle qu’elle a été introduite dans la version de DirectX 3,0.

Le format binaire est une représentation sous forme de jeton du format texte. Les jetons peuvent être autonomes ou accompagnés d’enregistrements de données primitifs. Les jetons autonomes donnent une structure grammaticale, et les jetons d’enregistrement fournissent les données nécessaires.

Notez que toutes les données sont stockées au format Little endian. Un flux de données binaires valide se compose d’un en-tête suivi de modèles et/ou d’objets de données.

Cette section décrit les composants suivants du format de fichier binaire et fournit un exemple de modèle et d’objet de données binaires.

-   [En-tête](header.md)
-   [Jetons](tokens.md)
-   [Enregistrements de jeton](token-records.md)
-   [Modèles](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [Données](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [Exemples](examples.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de format de fichier X](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



