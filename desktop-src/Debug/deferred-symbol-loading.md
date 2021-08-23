---
description: Pour économiser du temps et de la mémoire lors de l’utilisation de nombreux fichiers de symboles, utilisez la fonction SymSetOptions pour définir l’option de chargement différé des symboles ( \_ chargements différés SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Chargement de symboles différés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957148"
---
# <a name="deferred-symbol-loading"></a>Chargement de symboles différés

Pour économiser du temps et de la mémoire lors de l’utilisation de nombreux fichiers de symboles, utilisez la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) pour définir l’option de chargement différé des symboles ( \_ chargements différés SYMOPT \_ ), puis utilisez la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) ou [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) pour charger les symboles différés pour tous les modules. Le gestionnaire de symboles répertorie les symboles qui sont disponibles pour les modules, mais ne mappe pas les informations de débogage en mémoire tant qu’il n’est pas demandé. Il s’agit de la méthode recommandée pour utiliser efficacement les symboles de débogage. Toutes les fonctions qui utilisent des symboles sont affectées par le chargement de symboles différés.

 

 



