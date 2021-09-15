---
description: Le nom de la fonction PatBlt (abréviation pour le transfert de bloc de modèle) implique que cette fonction réplique simplement le pinceau (ou le modèle) jusqu’à ce qu’elle remplisse un rectangle spécifié.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transfert de bloc de modèle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531965"
---
# <a name="pattern-block-transfer"></a>Transfert de bloc de modèle

Le nom de la fonction [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (abréviation pour le transfert de bloc de modèle) implique que cette fonction réplique simplement le pinceau (ou le modèle) jusqu’à ce qu’elle remplisse un rectangle spécifié. Toutefois, la fonction est en fait bien plus puissante. Avant de répliquer le pinceau, il combine les données de couleur du modèle avec les données de couleur des pixels existants sur l’affichage vidéo à l’aide d’une opération de pixellisation (ROP). Une ROP est une opération au niveau du bit qui est appliquée aux bits des données de couleur pour le pinceau répliqué et les bits des données de couleur du rectangle cible sur le périphérique d’affichage. Il y a 256 trames ; Toutefois, la fonction **PatBlt** ne reconnaît que ceux qui nécessitent un modèle et une destination (pas ceux qui requièrent une source). Le tableau suivant identifie les opérations de tramage les plus courantes.



| ROP       | Description                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copie le modèle dans le bitmap de destination.                                       |
| PATINVERT | Associe le bitmap de destination au modèle à l’aide de l’opérateur booléen XOR. |
| DSTINVERT | Inverse le bitmap de destination.                                                     |
| NOIRCEUR | Transforme toutes les sorties en zéros binaires.                                                   |
| BLANCHEté | Transforme toutes les sorties en fichiers binaires.                                                    |



 

Pour plus d’informations, consultez [codes d’opération Raster](raster-operation-codes.md).

 

 



