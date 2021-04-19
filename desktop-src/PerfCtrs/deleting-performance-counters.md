---
description: Pour supprimer les compteurs de performance de vos applications du système, procédez comme suit.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Suppression de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530861"
---
# <a name="deleting-performance-counters"></a>Suppression de compteurs de performances

Pour supprimer les compteurs de performance de votre application du système, procédez comme suit.

1.  Utilisez l’outil **unlodctr** inclus avec l’ordinateur pour supprimer les données relatives aux compteurs du Registre. Notez que la clé de **performance** de l’application doit exister pour que l’outil **unlodctr** aboutisse. Pour plus d’informations, consultez [suppression des noms et des descriptions des compteurs du Registre](removing-counter-names-and-descriptions-from-the-registry.md).
2.  Supprimez les clés de **performances** et de **liaison** sous la clé **services** de l’application. Pour supprimer ces clés, utilisez l’utilitaire Regedt32.exe ou appelez [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
