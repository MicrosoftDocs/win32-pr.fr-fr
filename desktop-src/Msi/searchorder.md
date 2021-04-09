---
description: La définition de cette stratégie système par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869046"
---
# <a name="searchorder"></a>SearchOrder

La définition de cette [stratégie système](system-policy.md) par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources. Les types de sources sont les suivants :

« n » – réseau

« m » – média (CD-ROM ou DVD)

« u » – Uniform Resource Locator (URL)

Par exemple, pour effectuer une recherche dans les sources réseau en premier, les sources de média seconde et les sources d’URL, la valeur de cette stratégie est « NMU ». Pour omettre la recherche d’un type de source particulier, laissez la lettre correspondante de la valeur.

Si l’option SearchOrder n’est pas définie, l’ordre de recherche par défaut est Network, Media, puis URL.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**SZ de REG \_**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 



