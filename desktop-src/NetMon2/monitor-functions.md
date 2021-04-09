---
description: Cette section décrit les fonctions d’assistance que vous pouvez utiliser pour développer des analyses personnalisées.
ms.assetid: 2c019183-9823-4e34-bb41-cf35f2731b8f
title: Fonctions de surveillance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9391927104196e282d4438c0b047e233d61f3619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862854"
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



 

 

 



