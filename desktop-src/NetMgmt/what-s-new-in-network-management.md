---
title: Nouveautés de la gestion de réseau
description: Nouveautés de la gestion de réseau
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e857ae495491fb35cdd396f227034540ad8f208510b678c9a93eaa7d212230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983076"
---
# <a name="whats-new-in-network-management"></a>Nouveautés de la gestion de réseau

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 et Windows Server 2012

Microsoft Windows 8 introduit de nouvelles fonctionnalités de programmation de gestion de réseau. Ces nouveaux éléments étendent la capacité de gestion de réseau à créer des packages d’approvisionnement pour les opérations de jonction de domaine hors connexion lors de la configuration d’ordinateurs avec Windows 8.

Les nouvelles fonctions de gestion de réseau sont les suivantes :

-   [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

Voici les nouvelles structures de gestion de réseau :

-   [**paramètres d' \_ approvisionnement netsetup \_**](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [**\_Informations utilisateur \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

la fonction [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) a été améliorée sur Windows 8 pour prendre en charge un nouveau niveau d’informations et retourner une structure [**user \_ INFO \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) avec les informations de compte d’utilisateur pour un compte connecté à une identité Internet.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

Microsoft Windows 7 introduit de nouvelles fonctionnalités de programmation de gestion de réseau. ces éléments étendent la capacité de gestion de réseau à autoriser les opérations de jonction de domaine hors connexion lors de la configuration d’ordinateurs avec Windows 7.

Les nouvelles fonctions de gestion de réseau sont les suivantes :

-   [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

Les fonctions de gestion de réseau existantes suivantes ont été améliorées pour prendre en charge des options supplémentaires :

-   [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a>Windows Server 2003

Microsoft Windows Server 2003 introduit de nouvelles fonctionnalités de programmation de gestion de réseau. ces éléments étendent la capacité des opérations de gestion de réseau sur Windows Server 2003 et versions ultérieures.

## <a name="windows-xp"></a>Windows XP

Microsoft Windows XP introduit de nouvelles fonctionnalités de programmation de gestion de réseau. ces éléments étendent la capacité des opérations de gestion de réseau sur Windows XP et versions ultérieures.

Les nouvelles fonctions de gestion de réseau sont les suivantes :

-   [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




