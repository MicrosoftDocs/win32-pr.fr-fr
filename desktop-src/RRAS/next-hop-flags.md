---
title: Indicateurs de tronçon suivant
description: Indicateurs de tronçon suivant
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Suivant
- Indicateurs de tronçon suivant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dbad78f5f10d7a9d7bf42f694f7e2fb3109c03b92dccdb5f31697f5cf8988c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790392"
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



 

 

 




