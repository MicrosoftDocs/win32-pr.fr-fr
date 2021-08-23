---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93228857af2e531360b6238ab649daf8ac3f9eb2acf0aecfb12348b0ed990b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795239"
---
# <a name="exec"></a>Exec

**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Type de données | Plage                    | Valeur par défaut |
|-----------|--------------------------|---------------|
| SZ de REG \_   | *Chemin de l’exécutable* |               |



 

## <a name="browser-integration-steps"></a>Étapes d’intégration du navigateur

1.  Utilisez la fonction [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) pour déterminer si le diagnostic réseau est installé. S’il est installé, la clé **{e2e2dd38-d088-4134-82b7-f2ba38496583}** est présente.
2.  Utilisez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) pour récupérer le chemin d’accès du fichier exécutable de diagnostics du réseau à partir de l’entrée **Exec** .
3.  Affichez la page nouvelle erreur si le diagnostic est installé sur le système.
4.  Créez une extension de navigateur qui crée un élément de barre d’outils standard si le diagnostic est installé sur le système.
5.  Exécutez l’exécutable Diagnostics du réseau à l’aide du chemin d’accès récupéré à l’étape 2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des fonctionnalités des outils de diagnostic réseau](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
