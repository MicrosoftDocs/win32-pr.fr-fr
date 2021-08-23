---
description: Vous pouvez installer des assemblys côte à côte en tant qu’assemblys partagés ou en tant qu’assemblys privés. Pour plus d’informations, consultez Installation d’assemblys côte à côte en tant qu’assemblys privés et installation d’assemblys côte à côte en tant qu’assemblys partagés.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Installation d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2124b490d64427e80b5beee53d1221cba4d5e59a23dc2d72c2da6833e14a98cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142132"
---
# <a name="installing-side-by-side-assemblies"></a>Installation d’assemblys côte à côte

Vous pouvez installer des assemblys côte à côte en tant qu’assemblys [partagés](/windows/desktop/Msi/shared-assemblies) ou en tant qu' [assemblys privés](/windows/desktop/Msi/private-assemblies). Pour plus d’informations, consultez [installation d’assemblys côte à côte en tant qu’assemblys privés](installing-side-by-side-assemblies-as-private-assemblies.md) et [installation d’assemblys côte à côte en tant qu’assemblys partagés](installing-side-by-side-assemblies-as-shared-assemblies.md).

Notez les points suivants :

-   les assemblys installés dans le Global Assembly Cache par une installation à l’aide du [contexte d’installation](/windows/desktop/Msi/installation-context) par utilisateur ne sont pas protégés par Windows Protection des fichiers.
-   les assemblys installés dans le Global Assembly Cache par une installation à l’aide du contexte d' [installation](/windows/desktop/Msi/installation-context) par ordinateur sont protégés par Windows Protection des fichiers.

 

 
