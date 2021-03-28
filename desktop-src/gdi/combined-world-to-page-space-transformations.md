---
description: Les cinq transformations de la page universelle peuvent être combinées en une seule matrice 3 par 3.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Transformations de l’espace universel vers la page combinées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972738"
---
# <a name="combined-world-to-page-space-transformations"></a>Transformations de l’espace universel vers la page combinées

Les cinq transformations de la page universelle peuvent être combinées en une seule matrice 3 par 3. La fonction [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) peut être utilisée pour combiner deux espaces universels avec les transformations d’espace de page. Les transformations combinées peuvent être utilisées pour modifier la sortie associée à un contexte de périphérique (DC) particulier en appelant la fonction [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) et en fournissant les éléments de cette matrice. Quand une application appelle **SetWorldTransform**, elle stocke les éléments de la matrice 3 par 3 dans une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) . Les membres de cette structure correspondent aux deux premières colonnes d’une matrice 3 par 3 ; la dernière colonne de la matrice n’est pas requise, car ses valeurs sont constantes.

Les éléments de la matrice de transformation universelle actuelle peuvent être réactifs en appelant la fonction [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) et en fournissant un pointeur vers une structure [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .

 

 



