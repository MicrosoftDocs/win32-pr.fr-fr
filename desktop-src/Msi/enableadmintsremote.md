---
description: à partir de Windows Server 2008 et Windows Vista, cette stratégie n’a plus aucun effet.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091417"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

à partir de Windows Server 2008 et Windows Vista, cette stratégie n’a plus aucun effet. Un administrateur peut effectuer une installation à partir de la session de console d’un serveur Terminal Server. Un administrateur peut également effectuer une installation à partir d’une session client du serveur Terminal Server.

pour plus d’informations, consultez [Services Terminal server](/windows/desktop/TermServ/terminal-services-portal) dans le kit de développement logiciel (SDK) de Microsoft Windows.

* * systèmes d’exploitation antérieurs à Windows Server 2008 et Windows Vista : * *

La définition de cette [stratégie système](system-policy.md) par ordinateur permet aux administrateurs d’effectuer des installations à partir d’une session client du serveur Terminal Server. Si cette stratégie n’est pas définie, les administrateurs peuvent uniquement effectuer des installations à partir de la session de la console. Les utilisateurs non administratifs ne peuvent jamais effectuer des installations à partir d’une session client. La valeur par défaut de cette stratégie permet uniquement aux administrateurs d’effectuer des installations à partir de la session de la console. Les administrateurs peuvent toujours effectuer des [installations d’administration](administrative-installation.md) à partir d’une session cliente du serveur Terminal Server, ou à partir de la session de la console, que cette stratégie soit définie ou non.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

pour plus d’informations, voir aussi [utilisation de Windows Installer avec une Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
