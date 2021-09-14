---
description: en savoir plus sur les concepts de Windows Installer qui commencent par la lettre A, tels que l’accessibilité et la phase d’acquisition.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092982"
---
# <a name="a-windows-installer"></a>A (Windows Installer)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**aux**
</dt> <dd>

Implémentation de la conception pour rendre l’interface utilisateur du programme d’installation accessible à tous les utilisateurs. Pour plus d’informations sur l’accessibilité, consultez la rubrique de vue d’ensemble : [accessibilité](accessibility.md).

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**phase d’acquisition**
</dt> <dd>

Phase d’installation pendant laquelle le programme d’installation détermine la procédure. la phase d’Acquisition commence quand une application ou un utilisateur demande à [*Windows Installer*](m-gly.md) d’installer une application ou une fonctionnalité. Le programme d’installation interroge ensuite la [*base de données*](i-gly.md) à la recherche d’informations lors de la génération du [*script d’exécution*](e-gly.md) de l’installation. Pour plus d’informations sur les phases d’une installation, consultez [mécanisme d’installation](installation-mechanism.md).

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**transactionnel**
</dt> <dd>

la plupart des fonctions effectuées par Windows Installer sont encapsulées dans des actions. Chaque action spécifie l’exécution d’une fonction particulière et le déroulement total des procédures de l’installation est déterminé par la séquence d’actions dans les [*tables de séquence*](s-gly.md). les [*actions Standard*](s-gly.md) sont intégrées à Windows Installer. Les [*actions personnalisées*](c-gly.md) sont écrites par l’auteur du [*package*](p-gly.md)d’installation.

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Mode d’approbation Administrateur**
</dt> <dd>

État d’approbation activé par la protection de compte d’utilisateur (UAC) qui exécute tous les utilisateurs avec des privilèges minimum, y compris les administrateurs. Les utilisateurs doivent donner leur consentement pour élever les installations qui requièrent des privilèges d’administrateur.

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**supports**
</dt> <dd>

Capacité à rendre les interfaces nécessaires au chargement et à rendre une application disponible sans installer l’application. Lorsqu’un utilisateur ou une application active une interface publiée, le programme d’installation continue à installer les composants nécessaires. Les deux types de publicité sont l' [*attribution*](/windows) et la [*publication*](p-gly.md). Pour plus d’informations, consultez également [*Install-on-demand*](i-gly.md). Pour plus d’informations sur la façon dont le programme d’installation publie des applications, consultez [publication](advertisement.md).

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Service d’informations d’application (AIS)**
</dt> <dd>

service système de Windows Vista qui facilite le démarrage des installations nécessitant des privilèges élevés pour s’exécuter. Fournit l’interface utilisateur de consentement utilisée par le contrôle de compte d’utilisateur pour inviter un utilisateur à autoriser l’administrateur.

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**affectation**
</dt> <dd>

Rend une application disponible et la fait apparaître comme si elle avait été installée pour un utilisateur, sans l’installer réellement. L’attribution d’ajouter des raccourcis et des icônes au menu **Démarrer** , associe les fichiers appropriés et écrit les entrées de registre de l’application. Quand un utilisateur tente d’ouvrir une application affectée, le programme d’installation installe l’application. L’attribution et la [*publication*](p-gly.md) sont deux méthodes de [*publicité*](/windows). Pour plus d’informations, consultez [publication](advertisement.md).

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**exécution asynchrone**
</dt> <dd>

[*Action personnalisée*](c-gly.md) pendant laquelle le programme d’installation exécute simultanément des threads distincts de l’action personnalisée et de l’installation actuelle. Pour plus d’informations, consultez [actions personnalisées synchrones et asynchrones](synchronous-and-asynchronous-custom-actions.md).

</dd> </dl>

 

 
