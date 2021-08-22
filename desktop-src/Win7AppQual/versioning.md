---
description: contrôle de version (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: contrôle de version (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f029f5c3c17a481ddebe7976985ddff0f926fd162989a612e23af721b71c58e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994549"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>contrôle de version (Windows 7 et Windows Server 2008 R2-guide de qualité des applications)

l’un des problèmes les plus courants de compatibilité des applications pour Windows Internet Explorer est les chaînes de l’Agent utilisateur (UA) et les vecteurs de Version. Windows Internet Explorer 8 introduit une nouvelle chaîne UA pour aider les applications à détecter la version exécutée par les utilisateurs. En plus d’améliorer simplement la valeur MSIE associée à Internet Explorer dans la chaîne UA, Internet Explorer 8 ajoute une valeur Trident/4.0 pour vous aider à détecter si Internet Explorer 8 s’exécute en mode d’affichage de compatibilité. Ces modifications, ainsi que les vérifications de version codées en dur, peuvent potentiellement introduire des problèmes de compatibilité entre les navigateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



