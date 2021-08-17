---
description: Pour supprimer les compteurs de performance de vos applications du système, procédez comme suit.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Suppression de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144012"
---
# <a name="deleting-performance-counters"></a>Suppression de compteurs de performances

Pour supprimer les compteurs de performance de votre application du système, procédez comme suit.

1.  Utilisez l’outil **unlodctr** inclus avec l’ordinateur pour supprimer les données relatives aux compteurs du Registre. Notez que la clé de **performance** de l’application doit exister pour que l’outil **unlodctr** aboutisse. Pour plus d’informations, consultez [suppression des noms et des descriptions des compteurs du Registre](removing-counter-names-and-descriptions-from-the-registry.md).
2.  Supprimez les clés de **performances** et de **liaison** sous la clé **services** de l’application. Pour supprimer ces clés, utilisez l’utilitaire Regedt32.exe ou appelez [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
