---
description: La définition de cette stratégie système par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041039"
---
# <a name="searchorder"></a>SearchOrder

La définition de cette [stratégie système](system-policy.md) par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources. Les types de sources sont les suivants :

« n » – réseau

« m » – média (CD-ROM ou DVD)

« u » – Uniform Resource Locator (URL)

Par exemple, pour effectuer une recherche dans les sources réseau en premier, les sources de média seconde et les sources d’URL, la valeur de cette stratégie est « NMU ». Pour omettre la recherche d’un type de source particulier, laissez la lettre correspondante de la valeur.

Si l’option SearchOrder n’est pas définie, l’ordre de recherche par défaut est Network, Media, puis URL.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’utilisateur actuel programme d' \\  \\  \\  \\ **installation** de Microsoft Windows

## <a name="data-type"></a>Type de données

**SZ de REG \_**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> </dl>

 

 



