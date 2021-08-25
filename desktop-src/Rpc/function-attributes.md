---
title: Attributs de fonctions
description: Les attributs \ callback \ et \ local \ peuvent être appliqués en tant qu’attributs de fonction.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021019"
---
# <a name="function-attributes"></a>Attributs de fonctions

Les **\[** attributs de [**rappel**](/windows/desktop/Midl/callback) **\]** et **\[** [**locaux**](/windows/desktop/Midl/local) **\]** peuvent être appliqués en tant qu’attributs de fonction.

Un rappel est un appel distant du serveur au client qui s’exécute dans le cadre d’un thread d’exécution conceptuel. Un rappel est toujours émis dans le contexte d’un appel distant (ou rappel) et est exécuté par le thread qui a émis l’appel distant (ou rappel) d’origine.

Il est souvent préférable de placer une déclaration de procédure locale dans le fichier IDL, car il s’agit de l’emplacement logique pour décrire les interfaces à un package. L' **\[** [](/windows/desktop/Midl/local) **\]** attribut local indique qu’une déclaration de procédure n’est pas réellement une fonction distante, mais une procédure locale. Le compilateur MIDL ne génère pas de stub pour les fonctions avec l’attribut **\[ local \]** .

Il est important de noter qu’il n’est pas recommandé d’utiliser le **\[** [**rappel**](/windows/desktop/Midl/callback) **\]** dans la programmation multithread. En tant que fonction de programmation à thread unique, elle n’est pas conçue pour prendre en charge les demandes de sécurité fournies par un environnement multithread.

 

 