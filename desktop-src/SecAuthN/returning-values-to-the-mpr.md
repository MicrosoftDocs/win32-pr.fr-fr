---
description: les fonctions de mise en réseau Windows renvoient la \_ fonction WN réussite en cas de réussite ou elles retournent une valeur différente de zéro unique si la fonction rencontre une erreur. En outre, elles retournent des informations d’erreur étendues à l’aide de WNetSetLastError et SetLastError.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Retour de valeurs à l’MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbbb33a1666252178bd6cfb3c2fca33581149dfdab9e16512b60f82875719018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918894"
---
# <a name="returning-values-to-the-mpr"></a>Retour de valeurs à l’MPR

les fonctions de mise en réseau Windows renvoient la \_ fonction WN réussite en cas de réussite ou elles retournent une valeur différente de zéro unique si la fonction rencontre une erreur. En outre, elles retournent des informations d’erreur étendues à l’aide de [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) et [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror).

Pour prendre en charge le comportement ci-dessus, les fonctions de fournisseur réseau ne doivent pas appeler [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) avant de retourner. Cela est dû au fait que le MPR appelle **SetLastError** pour les fonctions de l’API du fournisseur réseau une fois qu’il a retourné. Si les fournisseurs de réseau appellent **SetLastError** directement, ils effectuent des appels de fonction redondants. Les fonctions des fournisseurs de réseau doivent simplement retourner un code d’erreur. Les codes d’erreur sont spécifiés dans la description de la fonction ou les [valeurs de retour](network-security-return-values.md). En outre, les fonctions du fournisseur de réseau peuvent retourner des [codes d’erreur système](../debug/system-error-codes.md), tels qu’une mémoire insuffisante. La seule exception est [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps), qui doit retourner un masque indiquant les fonctions prises en charge par le fournisseur réseau.

Si une fonction de fournisseur réseau doit retourner des informations d’erreur étendues, elle doit appeler [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora). cette fonction est fournie par le système d’exploitation Windows pour une utilisation par les fournisseurs de réseau. Lorsque le fournisseur appelle **WNetSetLastError**, il peut définir une chaîne contenant des informations supplémentaires sur l’erreur. Ces informations sont stockées par thread. cela est analogue à [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour les applications Windows. le système d’exploitation Windows appelle **WNetSetLastError** pour rechercher une chaîne stockée à l’aide de **WNetSetLastError** et, si elle est trouvée, retourne les informations d’erreur étendues à l’application appelante qui a initié la demande réseau.

> [!Note]  
> le préfixe WNet de [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) est trompeur, car cette api, contrairement à **WNetSetLastError**, ne fait pas partie du jeu d’api réseau Windows. **WNetSetLastError** est destiné à être utilisé uniquement par les fournisseurs de réseau. Le nom, **WNetSetLastError**, est conservé pour la compatibilité avec les fournisseurs existants.

 

 

 
