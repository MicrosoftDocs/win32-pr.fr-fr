---
description: Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Nettoyage du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956958"
---
# <a name="symbol-handler-cleanup"></a>Nettoyage du gestionnaire de symboles

Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Cette fonction énumère tous les modules chargés, libère chaque module et libère la mémoire allouée pour la liste de modules. Après avoir appelé **SymCleanup**, vous ne pouvez pas utiliser le handle de processus dans les fonctions de gestion de symboles tant que vous n’avez pas appelé la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



