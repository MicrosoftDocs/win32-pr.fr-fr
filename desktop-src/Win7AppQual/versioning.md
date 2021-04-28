---
description: Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103697"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Contrôle de version (Windows 7 et Windows Server 2008 R2-conseils de qualité des applications)

L’un des problèmes les plus courants de compatibilité des applications pour Windows Internet Explorer est l’agent utilisateur (UA), les chaînes et les vecteurs de version. Windows Internet Explorer 8 introduit une nouvelle chaîne UA pour aider les applications à détecter la version exécutée par les utilisateurs. En plus d’améliorer simplement la valeur MSIE associée à Internet Explorer dans la chaîne UA, Internet Explorer 8 ajoute une valeur Trident/4.0 pour vous aider à détecter si Internet Explorer 8 s’exécute en mode d’affichage de compatibilité. Ces modifications, ainsi que les vérifications de version codées en dur, peuvent potentiellement introduire des problèmes de compatibilité entre les navigateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



