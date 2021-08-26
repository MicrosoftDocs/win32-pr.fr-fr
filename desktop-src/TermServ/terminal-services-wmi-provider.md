---
title: Fournisseur WMI Services Bureau à distance
description: Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, fournisseur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4ed84dee9b2521c392b8b39ee1297121a85e1c4f8ad41f7d96d0d73042a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869599"
---
# <a name="remote-desktop-services-wmi-provider"></a>Fournisseur WMI Services Bureau à distance

Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.

la DLL du fournisseur est chargée par le processus de gestion de Windows (Winmgmt.exe) lorsqu’un client envoie une demande au serveur. L’administration est possible à l’aide des méthodes du fournisseur. Le fournisseur est inscrit à la fois comme instance et comme fournisseur de méthode.

Le fournisseur WMI Services Bureau à distance a été implémenté en tant que fournisseur dynamique dérivé de la classe de base du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) , en héritant de toutes ses propriétés et méthodes, et d’une bibliothèque de liens dynamiques in-process.

Pour plus d’informations, consultez la [services Bureau à distance référence du fournisseur WMI](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du fournisseur WMI Services Bureau à distance](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 