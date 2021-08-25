---
title: Détermination de la version de BITS sur un ordinateur
description: Pour déterminer la version de BITS sur l’ordinateur client, vérifiez la version de QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caa2c501fd5f37d44becf11679debb1390aeeb9ee47bee02b43a97788493cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005309"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Détermination de la version de BITS sur un ordinateur

Pour déterminer la version de BITS sur l’ordinateur client, vérifiez la version de QMgr.dll. Pour rechercher le numéro de version de la DLL :

-   Recherchez QMgr.dll dans% windir% \\ system32.
-   Cliquez avec le bouton droit sur QMgr.dll, puis cliquez sur **Propriétés**.
-   Cliquez sur l’onglet **version** .
-   Notez le numéro de version.

Vous pouvez également utiliser le code PowerShell suivant pour déterminer la version de l' .dll sur votre système :

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Si la DLL existe également dans% windir% \\ system32 \\ bits, répétez les étapes précédentes. BITS utilise la DLL avec le numéro de version le plus élevé.

Le tableau suivant répertorie les versions de BITS et leurs numéros de version de fichier QMgr.dll correspondants.



| Version de BITS | Numéro de version du fichier QMgr.dll |
|--------------|------------------------------|
| BITS 10,1    | 7.8. xxxx. xxxx                |
| BITS 5,0     | 7.7. xxxx. xxxx                |
| BITS 4,0     | 7.5. xxxx. xxxx                |
| BITS 3,0     | 7.0. xxxx. xxxx                |
| BITS 2.5     | 6.7. xxxx. xxxx                |
| BITS 2,0     | 6.6. xxxx. xxxx                |
| BITS 1,5     | 6,5. xxxx. xxxx                |
| BITS 1,2     | 6.2. xxxx. xxxx                |
| BITS 1,0     | 6.0. xxxx. xxxx                |



 

Vous pouvez également utiliser les identificateurs de classe symbolique pour déterminer la version de BITS qui est inscrite sur l’ordinateur. Le tableau suivant répertorie les versions de BITS et leurs identificateurs de classe symbolique correspondants. La fonction **CoCreateInstance** retourne **RegDB \_ E \_ CLASSNOTREG** si la classe n’est pas inscrite.



| Version de BITS  | Identificateur de classe symbolique         |
|---------------|-----------------------------------|
| BITS 10,1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5,0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4,0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3,0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2,0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1,5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1,2, 1,0 | CLSID \_ BackgroundCopyManager      |



 

 

 




