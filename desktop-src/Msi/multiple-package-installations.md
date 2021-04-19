---
description: Windows Installer pouvez installer plusieurs packages à l’aide du traitement des transactions.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Installations Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65fa30893f353d6661a7f77fe23fe55b4c9b22c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518422"
---
# <a name="multiple-package-installations"></a>Installations Multiple-Package

Windows Installer pouvez installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md). Cette fonctionnalité est disponible à partir de Windows Installer 4,5. Le programme d’installation installe tous les packages appartenant à une transaction à plusieurs packages ou aucun des packages. Si tous les packages de la transaction ne peuvent pas être installés avec succès, ou si l’utilisateur annule l’installation, les Windows Installer peuvent restaurer les modifications et restaurer l’ordinateur à son état d’origine.

Un package d’installation de plusieurs packages peut contenir une [table MsiEmbeddedChainer](msiembeddedchainer-table.md) qui fait référence à une fonction définie par l’utilisateur qui utilise les fonctions [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)et [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

Le [tableau MsiPackageCertificate](msipackagecertificate-table.md) répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent une installation de plusieurs packages. Vous pouvez utiliser ce tableau pour réduire le nombre de fois où votre installation de plusieurs packages affiche une invite de [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) qui requiert une réponse d’un administrateur.

Les fonctions de Windows Installer suivantes peuvent apporter des modifications à l’ordinateur de l’utilisateur lors de l’installation, de la réparation, de la mise à jour ou de la suppression des applications par le Windows Installer. À partir de Windows Installer 4,5, le programme d’installation peut restaurer les modifications apportées par ces fonctions lors du [*traitement transactionnel*](t-gly.md) d’une installation de plusieurs packages :

<dl>

[**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta)  
[**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)  
[**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)  
[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)  
[**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)  
[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)  
[**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)  
[**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)  
[**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)  
[**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)  
[**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)  
[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)  
[**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)  
[**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)  
[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)  
[**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)  
[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)  
</dl>

Il existe une exception si le Windows Installer rencontre un package appartenant à une installation de plusieurs packages qui contient une action [ForceReboot](forcereboot-action.md) ou [ScheduleReboot](schedulereboot-action.md) . Dans ce cas, Windows Installer n’installe pas uniquement ce package. D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md): * * le [*traitement transactionnel*](t-gly.md) d’installations Windows Installer à plusieurs packages n’est pas pris en charge. Ces versions du Windows Installer ne peuvent pas restaurer l’installation de plusieurs packages en tant que transaction unique.

**Windows Server 2008 R2 avec le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) activé :** Non pris en charge. L’installation de plusieurs packages à l’aide de la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) échoue si le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) est activé.

 

 
