---
description: Un gestionnaire de terminaisons garantit qu’un bloc de code spécifique est exécuté chaque fois que le contrôle de workflow quitte un corps de code protégé particulier. Un gestionnaire de terminaisons se compose des éléments suivants.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Gestion des arrêts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292958"
---
# <a name="termination-handling"></a>Gestion des arrêts

Un *Gestionnaire de terminaisons* garantit qu’un bloc de code spécifique est exécuté chaque fois que le contrôle de workflow quitte un corps de code protégé particulier. Un gestionnaire de terminaisons se compose des éléments suivants.

-   Corps protégé du code
-   Bloc de code d’arrêt à exécuter lorsque le workflow de contrôle quitte le corps protégé

Les gestionnaires de terminaisons sont déclarés dans une syntaxe spécifique au langage. À l’aide du compilateur d’optimisation Microsoft C/C++, elles sont implémentées à l’aide de **\_ \_ try** et **\_ \_ enfin**. Pour plus d’informations, consultez [syntaxe du gestionnaire](handler-syntax.md).

Le corps de code gardé peut être un bloc de code, un ensemble de blocs imbriqués ou une procédure ou une fonction entière. Chaque fois que le corps protégé est exécuté, le bloc de code d’arrêt est exécuté. La seule exception est lorsque le thread se termine pendant l’exécution du corps gardé (par exemple, si la fonction [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ou [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) est appelée à partir du corps protégé).

Le bloc de fin est exécuté lorsque le déroulement du contrôle quitte le corps protégé, que le corps protégé soit arrêté normalement ou anormalement. Le corps protégé est considéré comme terminé normalement lorsque la dernière instruction du bloc est exécutée et que le contrôle se poursuit de façon séquentielle dans le bloc de fin. Un arrêt anormal se produit lorsque le workflow de contrôle quitte le corps protégé en raison d’une exception ou en raison d’une instruction de contrôle telle que **Return**, **goto**, **break** ou **continue**. La fonction [**AbnormalTermination**](abnormaltermination.md) peut être appelée à partir du bloc de fin pour déterminer si le corps protégé s’est arrêté normalement.

 

 
