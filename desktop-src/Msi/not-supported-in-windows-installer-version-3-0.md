---
description: les Windows Installer fonctions, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 3.0 et versions antérieures.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: non pris en charge dans Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111018"
---
# <a name="not-supported-in-windows-installer-30"></a>non pris en charge dans Windows Installer 3,0

les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 3,0 et versions antérieures. L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge. consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière. pour plus d’informations sur les autres versions [de Windows Installer, consultez nouveautés de Windows Installer](what-s-new-in-windows-installer.md).

Windows le programme d’installation 3,0 est disponible pour Windows Server 2003, Windows XP ou Windows 2000. pour obtenir la liste de toutes les versions de Windows Installer et des fichiers redistribuables, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).

les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 3,0 et versions antérieures.

[Fonctions du programme d’installation](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Prototype de fonction de rappel

-   [**\_enregistrement du gestionnaire INSTALLUI \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tables de base de données](database-tables.md)

-   La colonne value de la [table MsiPatchMetadata](msipatchmetadata-table.md) accepte **OptimizedInstallMode** et **MinorUpdateTargetRTM**.

[Propriétés](properties.md)

-   [**Propriété Msix64**](msix64.md)

[Windows Programme d’installation sur les systèmes d’exploitation 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   La [**propriété Résumé du modèle**](template-summary.md) accepte la valeur x64.

[Évaluateurs de cohérence internes-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
