---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748757"
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

 

 
