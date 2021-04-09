---
description: Lorsqu’une erreur se produit, la plupart des fonctions système retournent un code d’erreur, généralement 0, NULL ou &\# 8211 ; 1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Code Last-Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950469"
---
# <a name="last-error-code"></a>Code Last-Error

Lorsqu’une erreur se produit, la plupart des fonctions système retournent un code d’erreur, généralement 0, **null** ou-1. De nombreuses fonctions système définissent également un code d’erreur supplémentaire appelé *dernier code d’erreur*. Ce code d’erreur est conservé séparément pour chaque thread en cours d’exécution. une erreur dans un thread ne remplace pas le dernier code d’erreur dans un autre thread. Toute fonction peut appeler la fonction [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) ou [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) pour définir le dernier code d’erreur du thread en cours. Ces fonctions sont principalement destinées aux bibliothèques de liens dynamiques (DLL), afin qu’elles puissent fournir des informations à l’application appelante. Notez que certaines fonctions appellent **SetLastError** ou **SetLastErrorEx** avec 0 quand elles réussissent, effaçant le code d’erreur défini par la dernière fonction ayant échoué, alors que d’autres ne le font pas.

Une application peut récupérer le dernier code d’erreur à l’aide de la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . le code d’erreur peut en savoir plus sur ce qui s’est réellement produit pour faire échouer la fonction. La documentation relative aux fonctions système indique les conditions dans lesquelles la fonction définit le dernier code d’erreur.

Le système définit un ensemble de codes d’erreur qui peuvent être définis en tant que codes de dernière erreur ou être retournés par ces fonctions. Les codes d’erreur sont des valeurs 32 bits (le bit 31 est le bit le plus significatif). Le bit 29 est réservé aux codes d’erreur définis par l’application ; aucun code d’erreur système n’a ce bit défini. Si vous définissez des codes d’erreur pour votre application, définissez ce bit pour indiquer que le code d’erreur a été défini par une application et que les codes d’erreur ne sont pas en conflit avec les codes d’erreur définis par le système. Pour plus d’informations, consultez WinError. h et [codes d’erreur système](system-error-codes.md).

 

 
