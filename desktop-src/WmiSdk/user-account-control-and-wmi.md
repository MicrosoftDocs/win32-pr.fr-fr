---
description: Le contrôle de compte d’utilisateur (UAC) affecte les données WMI retournées à partir d’un outil en ligne de commande, l’accès à distance et la façon dont les scripts doivent s’exécuter. Pour plus d’informations sur UAC, consultez Prise en main avec le contrôle de compte d’utilisateur.
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: Contrôle de compte d’utilisateur et WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534004"
---
# <a name="user-account-control-and-wmi"></a>Contrôle de compte d’utilisateur et WMI

Le contrôle de compte d’utilisateur (UAC) affecte les données WMI retournées à partir d’un outil en ligne de commande, l’accès à distance et la façon dont les scripts doivent s’exécuter. Pour plus d’informations sur UAC, consultez [prise en main avec le contrôle de compte d’utilisateur](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

Les sections suivantes décrivent les fonctionnalités du contrôle de compte d’utilisateur :

-   [Contrôle de compte d’utilisateur](#user-account-control-and-wmi)
-   [Compte nécessaire pour exécuter les outils de Command-Line WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Gestion des connexions à distance sous UAC](#handling-remote-connections-under-uac)
-   [Effet UAC sur les données WMI retournées aux scripts ou aux applications](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Rubriques connexes](#related-topics)

## <a name="user-account-control"></a>Contrôle de compte d'utilisateur

Sous UAC, les comptes du groupe Administrateurs local ont deux [*jetons d’accès*](/windows/desktop/SecGloss/a-gly), l’un avec des privilèges d’utilisateur standard et l’autre avec des privilèges d’administrateur. En raison du filtrage des jetons d’accès UAC, un script est normalement exécuté sous le jeton d’utilisateur standard, sauf s’il est exécuté « en tant qu’administrateur » en mode de privilège élevé. Tous les scripts n’ont pas besoin de privilèges d’administrateur.

Les scripts ne peuvent pas déterminer par programme s’ils s’exécutent sous un jeton de sécurité utilisateur standard ou un jeton d’administrateur. Le script peut échouer avec une erreur d’accès refusé. Si le script requiert des privilèges d’administrateur, il doit être exécuté en mode élevé. L’accès aux espaces de noms WMI diffère selon que le script est exécuté en mode élevé. Certaines opérations WMI, telles que l’obtention de données ou l’exécution de la plupart des méthodes, ne nécessitent pas que le compte soit exécuté en tant qu’administrateur. Pour plus d’informations sur les autorisations d’accès par défaut, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md) et [exécution des opérations privilégiées](executing-privileged-operations.md).

En raison du contrôle de compte d’utilisateur, le compte qui exécute le script doit être dans le groupe Administrateurs sur l’ordinateur local pour pouvoir s’exécuter avec des droits élevés.

Vous pouvez exécuter un script ou une application avec des droits élevés en effectuant l’une des méthodes suivantes :

**Pour exécuter un script en mode élevé**

1.  Ouvrez une fenêtre d’invite de commandes en cliquant avec le bouton droit sur invite de commandes dans le menu Démarrer, puis en cliquant sur **exécuter en tant qu’administrateur**.
2.  Planifiez l’exécution du script avec élévation de privilèges à l’aide de Planificateur de tâches. Pour plus d’informations, consultez [contextes de sécurité pour les tâches en cours d’exécution](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Exécutez le script à l’aide du compte administrateur intégré.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Compte nécessaire pour exécuter les outils de Command-Line WMI

Pour exécuter les [outils de Command-Line WMI](wmi-command-line-tools.md)suivants, votre compte doit être dans le groupe administrateurs et l’outil doit être exécuté à partir d’une invite de commandes avec élévation de privilèges. Le compte administrateur intégré peut également exécuter ces outils.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    La première fois que vous exécutez WMIC après l’installation du système, celle-ci doit être exécutée à partir d’une invite de commandes avec élévation de privilèges. Le mode avec élévation de privilèges peut ne pas être nécessaire pour les exécutions suivantes de WMIC, à moins que les opérations WMI requièrent des privilèges d’administrateur.

-   [**critique**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Pour exécuter le [*contrôle WMI*](gloss-w.md) (wmimgmt. msc) et apporter des modifications aux paramètres de sécurité ou d’audit de l’espace de noms WMI, votre compte doit disposer du droit modifier la sécurité explicitement accordé ou se trouver dans le groupe Administrateurs local. Le compte administrateur intégré peut également modifier la sécurité ou l’audit d’un espace de noms.

Wbemtest.exe, un outil de ligne de commande qui n’est pas pris en charge par les services de support technique Microsoft, peut être exécuté par des comptes qui ne se trouvent pas dans le groupe Administrateurs local, sauf si une opération spécifique requiert des privilèges normalement accordés aux comptes d’administrateur.

## <a name="handling-remote-connections-under-uac"></a>Gestion des connexions à distance sous UAC

Si vous vous connectez à un ordinateur distant dans un domaine ou dans un groupe de travail, déterminez si le filtrage UAC se produit.

Si votre ordinateur fait partie d’un domaine, connectez-vous à l’ordinateur cible à l’aide d’un compte de domaine qui se trouve dans le groupe Administrateurs local de l’ordinateur distant. Ensuite, le filtrage des jetons d’accès UAC n’affectera pas les comptes de domaine du groupe Administrateurs local. N’utilisez pas un compte local, sans domaine sur l’ordinateur distant, même si le compte se trouve dans le groupe administrateurs.

Dans un groupe de travail, le compte qui se connecte à l’ordinateur distant est un utilisateur local sur cet ordinateur. Même si le compte se trouve dans le groupe administrateurs, le filtrage UAC signifie qu’un script s’exécute en tant qu’utilisateur standard. Une meilleure pratique consiste à créer un compte d’utilisateur ou un groupe d’utilisateurs local dédié sur l’ordinateur cible spécifiquement pour les connexions à distance.

La sécurité doit être ajustée pour pouvoir utiliser ce compte, car le compte n’a jamais bénéficié de privilèges d’administrateur. Donnez à l’utilisateur local :

-   Exécution à distance et activation des droits d’accès à DCOM. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).
-   Droits d’accès à l’espace de noms WMI à distance (activation à distance). Pour plus d’informations, consultez [accès aux espaces de noms WMI](access-to-wmi-namespaces.md).
-   Droit d’accéder à l’objet sécurisable spécifique, en fonction de la sécurité requise par l’objet.

Si vous utilisez un compte local, soit parce que vous vous trouvez dans un groupe de travail, soit parce qu’il s’agit d’un compte d’ordinateur local, vous pouvez être contraint d’attribuer des tâches spécifiques à un utilisateur local. Par exemple, vous pouvez accorder à l’utilisateur le droit d’arrêter ou de démarrer un service spécifique par le biais de la commande SC.exe, des méthodes [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) et [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service), ou via stratégie de groupe à l’aide de gpedit. msc. Certains objets sécurisables ne permettent pas à un utilisateur standard d’effectuer des tâches et n’offrent aucun moyen de modifier la sécurité par défaut. Dans ce cas, vous devrez peut-être désactiver le contrôle de compte d’utilisateur afin que le compte d’utilisateur local ne soit pas filtré et devienne un administrateur complet. N’oubliez pas que pour des raisons de sécurité, la désactivation du contrôle de compte d’utilisateur doit être un dernier recours.

La désactivation du contrôle de compte d’utilisateur à distance en modifiant l’entrée de Registre qui contrôle le contrôle de compte d’utilisateur distant n’est pas recommandée, mais peut être nécessaire dans un groupe de travail. L’entrée de Registre est **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy**. Lorsque la valeur de cette entrée est égale à zéro (0), le filtrage des jetons d’accès UAC à distance est activé. Lorsque la valeur est 1, le contrôle de compte d’utilisateur distant est désactivé.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Effet UAC sur les données WMI retournées aux scripts ou aux applications

Si un script ou une application s’exécute sous un compte dans le groupe administrateurs, mais ne s’exécute pas avec un privilège élevé, vous risquez de ne pas obtenir toutes les données retournées, car ce compte s’exécute en tant qu’utilisateur standard. Les [*fournisseurs*](gloss-p.md) WMI pour certaines classes ne retournent pas toutes les instances à un compte d’utilisateur standard ou un compte d’administrateur qui ne s’exécute pas en tant qu’administrateur complet en raison du filtrage UAC.

Les classes suivantes ne retournent pas certaines instances lorsque le compte est filtré par UAC :

-   [**\_Bus Win32**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**\_Imprimante Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**\_ComponentCategory Win32**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**\_LogicalProgramGroupItem Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**\_LogicalProgramGroup Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**\_NetworkConnection Win32**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**\_UserAccount Win32**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**\_PrinterDriver Win32**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**\_PortResource Win32**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**\_DeviceMemoryAddress Win32**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

Les classes suivantes ne retournent pas de propriétés lorsque le compte est filtré par UAC :

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**\_DCOMApplicationSetting Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**\_DCOMApplication Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**\_Carte mère Win32**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**\_ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**\_NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**\_MotherboardDevice Win32**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**\_DiskDrive Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**\_PnPEntity Win32**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**\_VideoController Win32**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**\_ParallelPort Win32**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**\_Disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**\_SystemDriver Win32**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**\_IRQResource Win32**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**\_NetworkProtocol Win32**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> <dt>

[Accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Modification de la sécurité d’accès sur les objets sécurisables](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
