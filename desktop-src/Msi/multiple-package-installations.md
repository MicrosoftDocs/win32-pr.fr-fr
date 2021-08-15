---
description: Windows Le programme d’installation peut installer plusieurs packages à l’aide du traitement des transactions.
ms.assetid: c4a0f4d8-818d-4e60-908b-adaa2a54de95
title: Installations Multiple-Package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d525c2904d25fb06403f85914f2b04fce2ebc57f22801a2413b2f09ad1c396
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943410"
---
# <a name="multiple-package-installations"></a>Installations Multiple-Package

Windows Le programme d’installation peut installer plusieurs packages à l’aide du [*traitement des transactions*](t-gly.md). cette fonctionnalité est disponible à partir de Windows Installer 4,5. Le programme d’installation installe tous les packages appartenant à une transaction à plusieurs packages ou aucun des packages. si tous les packages de la transaction ne peuvent pas être installés avec succès, ou si l’utilisateur annule l’installation, les Windows Installer peuvent restaurer les modifications et restaurer l’ordinateur à son état d’origine.

Un package d’installation de plusieurs packages peut contenir une [table MsiEmbeddedChainer](msiembeddedchainer-table.md) qui fait référence à une fonction définie par l’utilisateur qui utilise les fonctions [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona), [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)et [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) .

Le [tableau MsiPackageCertificate](msipackagecertificate-table.md) répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent une installation de plusieurs packages. Vous pouvez utiliser ce tableau pour réduire le nombre de fois où votre installation de plusieurs packages affiche une invite de [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) qui requiert une réponse d’un administrateur.

les fonctions de Windows Installer suivantes peuvent apporter des modifications à l’ordinateur de l’utilisateur lors de l’installation, de la réparation, de la mise à jour ou de la suppression des applications par le Windows Installer. à partir de Windows Installer 4,5, le programme d’installation peut restaurer les modifications apportées par ces fonctions lors du [*traitement transactionnel*](t-gly.md) d’une installation de plusieurs packages :

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

il existe une exception si le Windows Installer rencontre un package appartenant à une installation de plusieurs packages qui contient une action [ForceReboot](forcereboot-action.md) ou [ScheduleReboot](schedulereboot-action.md) . dans ce cas, Windows Installer n’installe pas uniquement ce package. D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md): * * le [*traitement transactionnel*](t-gly.md) d’installations Windows Installer à plusieurs packages n’est pas pris en charge. ces versions du Windows Installer ne peuvent pas restaurer l’installation de plusieurs packages en tant que transaction unique.

**Windows Server 2008 R2 avec le rôle [Services Bureau à distance](../termserv/terminal-services-portal.md) activé :** Non pris en charge. L’installation de plusieurs packages à l’aide de la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) échoue si le rôle [services Bureau à distance](../termserv/terminal-services-portal.md) est activé.

 

 
