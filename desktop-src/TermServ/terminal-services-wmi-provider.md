---
title: Fournisseur WMI Services Bureau à distance
description: Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, fournisseur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031403"
---
# <a name="remote-desktop-services-wmi-provider"></a>Fournisseur WMI Services Bureau à distance

Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.

La DLL du fournisseur est chargée par le processus de gestion Windows (Winmgmt.exe) lorsqu’un client envoie une demande au serveur. L’administration est possible à l’aide des méthodes du fournisseur. Le fournisseur est inscrit à la fois comme instance et comme fournisseur de méthode.

Le fournisseur WMI Services Bureau à distance a été implémenté en tant que fournisseur dynamique dérivé de la classe de base du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) , en héritant de toutes ses propriétés et méthodes, et d’une bibliothèque de liens dynamiques in-process.

Pour plus d’informations, consultez la [services Bureau à distance référence du fournisseur WMI](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du fournisseur WMI Services Bureau à distance](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 