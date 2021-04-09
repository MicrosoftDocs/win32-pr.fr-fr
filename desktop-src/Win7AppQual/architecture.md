---
description: Internet Explorer (LCIE) faiblement couplé améliore la fiabilité du navigateur en séparant ses composants et en disserrant leur interdépendance.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Architecture (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760083"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Architecture (Windows 7 et Windows Server 2008 R2-Guide pratique de la qualité des applications)

*Internet Explorer (LCIE) faiblement couplé* améliore la fiabilité du navigateur en séparant ses composants et en disserrant leur interdépendance.

En particulier, LCIE essaie d’isoler le cadre Windows Internet Explorer et ses onglets dans des processus distincts. Dans Windows Internet Explorer 8, cette isolation améliore les performances et l’extensibilité. Ce changement architectural peut affecter la compatibilité des extensions et des modules complémentaires, y compris les contrôles ActiveX, les objets application d’assistance du navigateur et les composants de barre d’outils d’interface utilisateur qui sont générés à l’aide de techniques de programmation plus anciennes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concevoir des mises à jour qui ont un impact sur la compatibilité entre les navigateurs](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



