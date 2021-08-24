---
description: Crypt32.dll est le module qui implémente la plupart des fonctions CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versions de Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88fed9fb7e31af86673c4d24a9dd828c8d690441986725026f982c0720753c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876469"
---
# <a name="crypt32dll-versions"></a>Versions de Crypt32.dll

Crypt32.dll est le module qui implémente un grand nombre des fonctions de certificat et de messagerie de chiffrement dans l’CryptoAPI, telles que [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll est un module fourni avec les systèmes d’exploitation Windows et Windows Server, mais les différentes versions de cette DLL offrent des fonctionnalités différentes. Il n’existe aucune API pour déterminer la version de CryptoAPI en cours d’utilisation, mais vous pouvez déterminer la version de Crypt32.dll en cours d’utilisation à l’aide des fonctions [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) et [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

En général, les plages de versions de Crypt32.dll correspondent aux versions de système d’exploitation, comme indiqué dans le tableau suivant. Toutefois, cette table doit être utilisée comme indication uniquement parce qu’il est possible, par le biais d’autres moyens de mise à jour, que la version du Crypt32.dll diffère de celle indiquée dans le tableau.

| Version de Crypt32.dll                               | Système d’exploitation                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *version* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *version* >= 5.131.2600.1243                   | Windows xp avec service pack 2 (SP2) Windows xp avec service pack 1 (SP1) avec le correctif [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *version* < 5.131.2600.1243 | Windows XP avec SP1Windows XP<br/>                                                                                                                                        |



 

 

 
