---
description: Vous pouvez utiliser Win32 \_ Process. Create pour exécuter un script ou une application sur un ordinateur distant. Toutefois, pour des raisons de sécurité, le processus ne peut pas être interactif. Lorsque \_ le processus Win32. Create est appelé sur l’ordinateur local, le processus peut être interactif.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Création de processus à distance à l’aide de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526232"
---
# <a name="creating-processes-remotely-using-wmi"></a>Création de processus à distance à l’aide de WMI

Vous pouvez utiliser [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) pour exécuter un script ou une application sur un ordinateur distant. Toutefois, pour des raisons de sécurité, le processus ne peut pas être interactif. Lorsque **le \_ processus Win32. Create** est appelé sur l’ordinateur local, le processus peut être interactif.

> [!WARNING]
> Cette rubrique décrit la procédure générale à respecter pour créer un processus distant avec WMI. si vous cherchez simplement à exécuter un script sur un système distant, consultez [connexion à wmi à distance à partir de Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)ou [connexion à wmi sur un ordinateur distant à l’aide de Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Pour plus d’informations générales sur la communication à distance avec PowerShell, consultez [exécution de commandes distantes](https://technet.microsoft.com/library/dd819505.aspx).

 

Le processus distant n’a pas d’interface utilisateur, mais il est listé dans le **Gestionnaire des tâches**. Un processus créé localement peut s’exécuter sous n’importe quel compte si le compte dispose de l’autorisation **Execute Method** pour l' \\ espace de noms CIMV2 racine. Un processus créé à distance peut s’exécuter sous n’importe quel compte si le compte a la **méthode Execute** et les autorisations **Remote Enable** pour la racine \\ cimv2. La **méthode Execute** et les autorisations **Remote Enable** sont définies dans le contrôle WMI dans le panneau de configuration. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).

Vous pouvez utiliser [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) pour créer un processus interactif à distance. Mais les processus démarrés par **Win32 \_ ScheduledJob. Create** s’exécutent sous le compte LocalSystem qui peut confère un trop grand privilège.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Connexion à un troisième ordinateur-délégation](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
