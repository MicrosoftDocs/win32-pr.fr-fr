---
title: Substituts de DLL
description: Substituts de DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512278"
---
# <a name="dll-surrogates"></a>Substituts de DLL

COM permet de créer des serveurs DLL qui peuvent être chargés dans un processus EXE de substitution. Cela combine la facilité d’écriture des serveurs DLL avec les avantages de l’implémentation de l’exécutable. Les outils de développement comme Microsoft Visual Studio faciliter l’écriture de serveurs DLL, mais un serveur DLL en lui-même a des limites. L’exécution du serveur de DLL dans un processus de substitution offre plusieurs avantages possibles :

-   Isolation des erreurs et possibilité de traiter plusieurs clients simultanément.
-   Dans un environnement distribué, une implémentation de serveur DLL peut être utilisée pour traiter les clients distants.
-   Cela peut permettre aux clients de se protéger eux-mêmes du code du serveur non approuvé tout en leur permettant d’accéder aux services fournis par le serveur de DLL.
-   L’exécution d’un serveur DLL dans un substitut fournit la DLL avec la sécurité du substitut.

COM fournit un processus de substitution par défaut, ou vous pouvez écrire un substitut personnalisé si vous avez des besoins spéciaux.

Les rubriques suivantes fournissent plus d’informations sur les substituts de DLL :

-   [Configuration requise du serveur DLL](dll-server-requirements.md)
-   [Utilisation du substitut System-Supplied](using-the-system-supplied-surrogate.md)
-   [Écriture d’un substitut personnalisé](writing-a-custom-surrogate.md)

 

 




