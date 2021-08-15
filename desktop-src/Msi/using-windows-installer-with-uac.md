---
description: Windows le programme d’installation est conforme au contrôle de compte d’utilisateur (UAC) dans Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: utilisation de Windows Installer avec UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458d6265938f44a694366e8145d60aa5d031d47e715932502bd1b82e7012b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942279"
---
# <a name="using-windows-installer-with-uac"></a>utilisation de Windows Installer avec UAC

Windows le programme d’installation est conforme au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) dans Windows Vista. avec l’autorisation d’un administrateur, les Windows Installer peuvent installer des applications ou des correctifs pour le compte d’un utilisateur qui n’est peut-être pas membre du groupe administrateurs. c’est ce qu’on appelle une installation [*avec élévation de privilèges*](e-gly.md) , car le Windows Installer apporte des modifications au système pour le compte de l’utilisateur, qui ne seraient normalement pas autorisées si l’utilisateur effectuait les modifications directement.

-   lorsque vous utilisez Windows Vista dans un environnement d’entreprise, les applications peuvent être désignées en tant qu’applications gérées. À l’aide du déploiement et de la [stratégie de groupe](/previous-versions/windows/desktop/Policy/group-policy-start-page)de l’application, les administrateurs peuvent verrouiller les répertoires, puis affecter ou publier les applications gérées dans ces répertoires à des [*utilisateurs standard*](s-gly.md) pour l’installation, la réparation ou la suppression. Les applications managées sont inscrites dans la ruche de Registre **HKEY \_ local \_ machine** . Une fois qu’une application a été inscrite en tant qu’application gérée, les opérations d’installation suivantes s’exécutent toujours avec des privilèges élevés. Si l’utilisateur s’exécute en tant qu’administrateur, aucune invite n’est requise pour poursuivre l’installation. Si l’utilisateur s’exécute en tant qu’utilisateur standard et que l’application a déjà été affectée ou publiée, l’installation de l’application managée peut continuer sans invite.
-   lorsque vous utilisez Windows Vista dans un environnement autre que l’environnement d’entreprise, le contrôle de compte d’utilisateur gère l’élévation de l’installation de l’application. Windows Le programme d’installation 4,0 peut appeler le [*service d’informations d’application*](a-gly.md) (AIS) pour demander l’autorisation de l’administrateur pour élever une installation. Avant qu’une installation identifiée comme nécessitant des privilèges d’administrateur puisse être exécutée, l’UAC invite l’utilisateur à donner son consentement pour élever l’installation. L’invite de consentement s’affiche par défaut, même si l’utilisateur est membre du groupe Administrateurs local, car les administrateurs s’exécutent en tant qu’utilisateurs standard jusqu’à ce qu’une application ou un composant système nécessitant des informations d’identification d’administration demande l’autorisation d’exécuter. Cette expérience utilisateur est appelée le [*mode d’approbation Administrateur*](a-gly.md) (AAM). Si un utilisateur standard tente d’installer l’application, il doit obtenir des privilèges d’administrateur pour lui fournir les informations d’identification d’administrateur pour continuer l’installation. Cette expérience utilisateur s’appelle une invite d’informations d’identification [*sur l’épaule*](o-gly.md) (OTS).
-   étant donné que le contrôle de compte d’utilisateur restreint les privilèges pendant les étapes d’une installation, les développeurs de packages de Windows Installer ne doivent pas supposer que leur installation aura toujours accès à toutes les parties du système. Windows les développeurs de packages d’installation doivent donc respecter les instructions de package décrites dans [les instructions](guidelines-for-packages.md) relatives aux Packages pour s’assurer que leur package fonctionne avec le contrôle de compte d’utilisateur et Windows Vista. Un package qui a été créé et testé pour se conformer au contrôle de compte d’utilisateur doit contenir la propriété [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) définie sur 1.
-   Un administrateur peut également utiliser les méthodes décrites dans la section : [installation d’un package avec des privilèges élevés pour un non-](installing-a-package-with-elevated-privileges-for-a-non-admin.md) administrateur pour permettre à un utilisateur non-administrateur d’installer une application avec des privilèges système élevés.
-   des privilèges sont requis pour installer une application dans le contexte géré par l’utilisateur. par conséquent, les Windows Installer réinstallations ou réparations de l’application sont également effectuées par le programme d’installation à l’aide de privilèges élevés. Cela signifie que seuls les correctifs de sources approuvées peuvent être appliqués à une application dans l’état géré par l’utilisateur. à partir de Windows Installer 3,0, vous pouvez appliquer un correctif à une application gérée par utilisateur une fois que le correctif a été inscrit comme ayant des privilèges élevés. Pour plus d’informations, consultez Mise à [jour corrective des Applications Per-User gérées](patching-per-user-managed-applications.md).

> [!Note]  
> lorsque des privilèges élevés ne sont pas requis pour installer un package Windows Installer, l’auteur du package peut supprimer la boîte de dialogue affichée par UAC pour demander aux utilisateurs l’autorisation d’administrateur. Pour plus d’informations, consultez [création de packages sans la boîte de dialogue contrôle de compte d’utilisateur](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
