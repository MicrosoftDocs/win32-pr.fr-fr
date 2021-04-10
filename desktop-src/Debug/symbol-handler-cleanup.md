---
description: Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Nettoyage du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860925"
---
# <a name="symbol-handler-cleanup"></a>Nettoyage du gestionnaire de symboles

Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Cette fonction énumère tous les modules chargés, libère chaque module et libère la mémoire allouée pour la liste de modules. Après avoir appelé **SymCleanup**, vous ne pouvez pas utiliser le handle de processus dans les fonctions de gestion de symboles tant que vous n’avez pas appelé la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



