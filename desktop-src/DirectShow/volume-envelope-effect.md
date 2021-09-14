---
description: Effet d’enveloppe de volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effet d’enveloppe de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238896"
---
# <a name="volume-envelope-effect"></a>Effet d’enveloppe de volume

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’effet enveloppe du volume définit le volume sur un flux audio.

ID de classe (CLSID) : {036A9790-C153-11D2-9EF7-006008039E37}

Nom de la variable CLSID : CLSID \_ AudMixer

Propriétés



| Propriété | Type   | Default | Description                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| Vol      | double | 1.0     | Volume, en pourcentage du volume créé. Vous pouvez produire des disparitions audio en faisant varier cette valeur de propriété au fil du temps. |



 

## <a name="remarks"></a>Notes

Chaque objet dans une chronologie peut avoir un seul effet d’enveloppe de volume. Dans une composition ou un groupe, l’enveloppe de volume est appliquée en premier, avant tout autre effet audio, quelle que soit sa priorité. Dans une source ou une piste, l’effet de volume est appliqué en fonction de sa priorité.

 

 



