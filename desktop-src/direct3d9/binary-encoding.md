---
description: Cette section détaille la version binaire du format de fichier DirectX (. x), telle qu’elle a été introduite dans la version de DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Encodage Binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515920"
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

 

 



