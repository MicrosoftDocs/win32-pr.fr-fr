---
description: Crypt32.dll est le module qui implémente la plupart des fonctions CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versions de Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750924"
---
# <a name="crypt32dll-versions"></a>Versions de Crypt32.dll

Crypt32.dll est le module qui implémente un grand nombre des fonctions de certificat et de messagerie de chiffrement dans l’CryptoAPI, telles que [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll est un module fourni avec les systèmes d’exploitation Windows et Windows Server, mais les différentes versions de cette DLL offrent des fonctionnalités différentes. Il n’existe aucune API pour déterminer la version de CryptoAPI en cours d’utilisation, mais vous pouvez déterminer la version de Crypt32.dll en cours d’utilisation à l’aide des fonctions [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) et [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

En général, les plages de versions de Crypt32.dll correspondent aux versions de système d’exploitation, comme indiqué dans le tableau suivant. Toutefois, cette table doit être utilisée comme indication uniquement parce qu’il est possible, par le biais d’autres moyens de mise à jour, que la version du Crypt32.dll diffère de celle indiquée dans le tableau.

| Version de Crypt32.dll                               | Système d’exploitation                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *version* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *version* >= 5.131.2600.1243                   | Windows XP avec Service Pack 2 (SP2) Windows XP avec Service Pack 1 (SP1) avec correctif [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *version* < 5.131.2600.1243 | Windows XP avec SP1Windows XP<br/>                                                                                                                                        |



 

 

 
