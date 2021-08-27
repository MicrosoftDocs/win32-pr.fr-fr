---
title: Substituts de DLL
description: Substituts de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808efe4a431a703282a705000d2fe18f6b4cfcde121d95c39fe65541b0260503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993249"
---
# <a name="dll-surrogates"></a>Substituts de DLL

COM permet de créer des serveurs DLL qui peuvent être chargés dans un processus EXE de substitution. Cela combine la facilité d’écriture des serveurs DLL avec les avantages de l’implémentation de l’exécutable. les outils de développement comme Microsoft Visual Studio faciliter l’écriture de serveurs dll, mais un serveur dll en lui-même a des limites. L’exécution du serveur de DLL dans un processus de substitution offre plusieurs avantages possibles :

-   Isolation des erreurs et possibilité de traiter plusieurs clients simultanément.
-   Dans un environnement distribué, une implémentation de serveur DLL peut être utilisée pour traiter les clients distants.
-   Cela peut permettre aux clients de se protéger eux-mêmes du code du serveur non approuvé tout en leur permettant d’accéder aux services fournis par le serveur de DLL.
-   L’exécution d’un serveur DLL dans un substitut fournit la DLL avec la sécurité du substitut.

COM fournit un processus de substitution par défaut, ou vous pouvez écrire un substitut personnalisé si vous avez des besoins spéciaux.

Les rubriques suivantes fournissent plus d’informations sur les substituts de DLL :

-   [Configuration requise du serveur DLL](dll-server-requirements.md)
-   [Utilisation du substitut System-Supplied](using-the-system-supplied-surrogate.md)
-   [Écriture d’un substitut personnalisé](writing-a-custom-surrogate.md)

 

 




