---
title: Compresseurs User-Selected
description: Compresseurs User-Selected
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Gestionnaire de compression vidéo (VCM), compresseurs sélectionnés par l’utilisateur
- VCM (gestionnaire de compression vidéo), compresseurs sélectionnés par l’utilisateur
- ICCompressorChoose fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370799"
---
# <a name="user-selected-compressors"></a>Compresseurs User-Selected

Lorsque vous compressez des données, votre application peut utiliser la fonction [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) pour créer une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le compresseur. Vous pouvez spécifier des indicateurs pour cette fonction pour permettre à l’utilisateur de spécifier la fréquence d’image clé et le débit de données, ou d’afficher une fenêtre d’aperçu.

Le compresseur sélectionné par l’utilisateur est automatiquement ouvert et son descripteur est retourné dans le membre hic de la structure [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) spécifiée dans **ICCompressorChoose**.

Si vous utilisez **ICCompressorChoose**, utilisez la fonction [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) pour fermer le compresseur et libérer toutes les ressources associées à la structure **COMPVARS** .

 

 




