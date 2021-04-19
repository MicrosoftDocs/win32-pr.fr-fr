---
description: À compter de Windows Server 2008, le fournisseur de fonctionnalités serveur fournit des informations sur les composants serveur installés sur le serveur. Cette classe permet aux administrateurs d’inventorier et de gérer leurs rôles serveur et leurs fonctionnalités.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Fournisseur de fonctionnalités serveur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534307"
---
# <a name="server-feature-provider"></a>Fournisseur de fonctionnalités serveur

À compter de Windows Server 2008, le fournisseur de fonctionnalités serveur fournit des informations sur les composants serveur installés sur le serveur. Cette classe permet aux administrateurs d’inventorier et de gérer leurs rôles serveur et leurs fonctionnalités.

Un rôle de serveur est défini comme un groupe de composants qui fournissent des fonctions pour une zone de fonctionnalités spécifique, telles que l’impression, les fichiers, le contrôle de domaine, etc. Les rôles de serveur classiques sont serveur de fichiers, serveur de messagerie, serveur DNS, contrôleur de domaine, serveur d’applications, etc.

Si une entreprise n’exécute pas de logiciel de gestion qui signale des rôles de serveur, par exemple Microsoft Operations Manager avec les packs d’administration installés, vous pouvez obtenir ces informations en interrogeant la classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) . Les informations sur les fonctionnalités et les rôles serveur des ordinateurs distants sont disponibles via des connexions à distance WMI normales ou à l’aide du service Windows Remote Management (WinRM). Pour plus d’informations sur les connexions WMI DCOM à distance, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md). Pour plus d’informations sur les connexions utilisant le protocole [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , consultez [Windows Remote Management](/windows/desktop/WinRM/portal).

Le fournisseur de fonctionnalités serveur prend en charge les classes WMI suivantes :

-   [**\_ServerFeature Win32**](win32-serverfeature.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](wmi-providers.md)
</dt> </dl>

 

 
