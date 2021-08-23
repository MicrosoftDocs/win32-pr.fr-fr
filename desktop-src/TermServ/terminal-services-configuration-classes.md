---
title: Services Bureau à distance les classes de configuration
description: Le fournisseur WMI de configuration Services Bureau à distance fournit les classes suivantes. Une illustration suit.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40784e1e0c9e0387b8d6ff60193639032f7e0cbe5e34c4a8b35aeb32cc37cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000123"
---
# <a name="remote-desktop-services-configuration-classes"></a>Services Bureau à distance les classes de configuration

Le fournisseur WMI de configuration Services Bureau à distance fournit les classes suivantes. Une illustration suit.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

Représente l’association entre les éléments système managés et la classe de paramètres définie pour eux.

</dd> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dd>

Classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

Classe de base pour la hiérarchie des éléments système.

</dd> <dt>

[**\_Paramètre CIM**](cim-setting.md)
</dt> <dd>

Représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.

</dd> <dt>

[**\_Terminal Win32**](win32-terminal.md)
</dt> <dd>

représente un terminal.

</dd> <dt>

[**\_TerminalError Win32**](win32-terminalerror.md)
</dt> <dd>

Représente une erreur de terminal.

</dd> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dd>

une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) . [**Win32 \_ TerminalService**](win32-terminalservice.md) représente la propriété d' **élément** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

</dd> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> <dd>

représente la configuration d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

</dd> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dd>

représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et le paramètre d’une propriété [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) particulière.

</dd> <dt>

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> <dd>

représente les paramètres qui peuvent être appliqués à un terminal.

</dd> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> <dd>

représente l’association entre un terminal et ses paramètres de configuration.

</dd> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> <dd>

autorise la suppression d’un compte qui existe sur [**le \_ Terminal Win32**](win32-terminal.md) et la modification des autorisations existantes.

</dd> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> <dd>

définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) associée à la stratégie de connexion.

</dd> <dt>

[**\_TSDiscoveredLicenseServer Win32**](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

Fournit des détails sur le serveur de licences Bureau à distance détecté.

</dd> <dt>

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> <dd>

définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris la stratégie de programme initiale.

</dd> <dt>

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> <dd>

représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.

</dd> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> <dd>

définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) relative à l’ouverture de session client.

</dd> <dt>

[**\_TSNetworkAdapterListSetting Win32**](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

énumère la liste des cartes réseau qui peuvent être configurées pour un [**\_ Terminal Win32**](win32-terminal.md), selon le protocole terminal et la méthode de transport spécifiés.

</dd> <dt>

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> <dd>

définit différents paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris les propriétés associées à la carte réseau et le nombre maximal de connexions autorisées.

</dd> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> <dd>

comprend une méthode pour ajouter de nouveaux comptes au terminal et une méthode pour restaurer les autorisations par défaut sur un terminal.

</dd> <dt>

[**\_TSRemoteControlSetting Win32**](win32-tsremotecontrolsetting.md)
</dt> <dd>

définit les paramètres de configuration du contrôle à distance pour la classe de [**\_ Terminal Win32**](win32-terminal.md) .

</dd> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dd>

Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

</dd> <dt>

[**\_TSSessionDirectorySetting Win32**](win32-tssessiondirectorysetting.md)
</dt> <dd>

Représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et une instance de la classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .

</dd> <dt>

[**\_TSSessionSetting Win32**](win32-tssessionsetting.md)
</dt> <dd>

définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , tels que les limites de temps, les actions de déconnexion et de reconnexion.

</dd> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> <dd>

Définit les paramètres de virtualisation IP (Internet Protocol) pour un serveur hôte de session Bureau à distance.

</dd> <dt>

[**\_TSVirtualIPSetting Win32**](win32-tsvirtualipsetting.md)
</dt> <dd>

Représente l’association entre une classe d’élément [**Win32 \_ TerminalService**](win32-terminalservice.md) et une classe de paramètre [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .

</dd> </dl>

L’illustration suivante montre les relations entre ces classes.

![relations entre les classes prises en charge](images/tswmi.png)

 

 