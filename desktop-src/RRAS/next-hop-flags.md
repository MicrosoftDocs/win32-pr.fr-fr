---
title: Indicateurs de tronçon suivant
description: Indicateurs de tronçon suivant
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Suivant
- Indicateurs de tronçon suivant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029696"
---
# <a name="next-hop-flags"></a>Indicateurs de tronçon suivant

## <a name="next-hop-state-flags"></a>Indicateurs d’état de tronçon suivant



| Constante                     | Valeur | Description                              |
|------------------------------|-------|------------------------------------------|
| État du tronçon de la version RTM \_ \_ \_ créé | 0     | Indique que le tronçon suivant a été créé. |
| État du tronçon de la version RTM \_ \_ \_ supprimé | 1     | Indique que le tronçon suivant a été supprimé. |



 

## <a name="next-hop-flags"></a>Indicateurs de tronçon suivant



| Constante                    | Valeur  | Description                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_indicateurs tronçons RTM \_ \_ distants | 0x0001 | Ce tronçon suivant pointe vers une destination distante qui n’est pas directement accessible. Pour obtenir le chemin d’accès complet, le client doit effectuer une recherche récursive. |
| \_indicateurs de tronçons de \_ \_ la version RTM   | 0x0002 | Cet indicateur est réservé à une utilisation ultérieure.                                                                                                                 |



 

## <a name="next-hop-added"></a>Tronçon suivant ajouté



| Constante                  | Valeur | Description                 |
|---------------------------|-------|-----------------------------|
| \_ \_ nouvelle modification du tronçon RTM \_ | 0x01  | Un nouveau tronçon suivant a été créé. |



 

 

 




