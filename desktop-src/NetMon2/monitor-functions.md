---
description: Cette section décrit les fonctions d’assistance que vous pouvez utiliser pour développer des analyses personnalisées.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Fonctions de surveillance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a46aff05c9d8775edf5bb233cb18f288dc7ba4d65ba0300370ee7ede3a2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677099"
---
# <a name="monitor-functions"></a>Fonctions de surveillance

Cette section décrit les fonctions d’assistance que vous pouvez utiliser pour développer des analyses personnalisées.



| Fonction                                       | Description                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllGetMonitorObject](dllgetmonitorobject.md) | Crée une instance de l’analyse.                                                                                                                              |
| [HTMLValueToUnicode](htmlvaluetounicode.md)   | Convertit une \_ chaîne de version html FP UTF8 en Unicode.                                                                                                             |
| [LoadDWORD](loaddword.md)                     | Charge un **DWORD** à partir d’une chaîne de configuration html.                                                                                                             |
| [LoadIPAddresses](loadipaddresses.md)         | Charge une liste d’adresses IP à partir d’une chaîne de configuration TEXTAREA HTML.                                                                                             |
| [LoadIPXAddresses](loadipxaddresses.md)       | Charge une liste d’adresses IPX à partir d’une chaîne de configuration TEXTAREA HTML.                                                                                            |
| [LoadMACAddresses](loadmacaddresses.md)       | Charge une liste d’adresses MAC à partir d’une chaîne de configuration TEXTAREA HTML.                                                                                             |
| [LoadStringAddr](loadstringaddr.md)           | Transforme une chaîne (telle que « 157.54.32.45 ») en une adresse **DWORD** .                                                                                             |
| [LoadTCHAR](loadtchar.md)                     | Recherche un nom de variable demandé dans la chaîne de configuration et alloue suffisamment d’espace (à l’aide de **HeapAllocMemory**) pour le stocker, le copier et le retourner. |
| [OnLoadingDLL](onloadingdll.md)               | Indique que le chargement de la DLL a commencé. Le MCSVC appelle cette fonction lors du premier chargement de la DLL du moniteur.                                                     |



 

 

 



