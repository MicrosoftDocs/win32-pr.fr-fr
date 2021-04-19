---
description: Cette stratégie système par ordinateur désactive la création de points de contrôle par Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544671"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Cette [stratégie système](system-policy.md) par ordinateur désactive la création de points de contrôle par Windows Installer.

Si la valeur est 0 ou absente, le programme d’installation effectue un point de contrôle normal pour l’installation ou la désinstallation. Si la valeur est 1, le programme d’installation ne crée aucun point de contrôle.

Cette stratégie affecte uniquement les points de contrôle définis par Windows Installer. Sur les ordinateurs Windows XP, les administrateurs peuvent décider de désactiver les points de contrôle à partir de Windows Installer pour améliorer les performances. La [**restauration du système**](../sr/system-restore-portal.md) crée également des points de contrôle supplémentaires. Pour plus d’informations, consultez [points de restauration système et le Windows Installer](system-restore-points-and-the-windows-installer.md) et [définition d’un point de restauration à partir d’une action personnalisée](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Clé de Registre

Définissez la valeur nommée LimitSystemRestoreCheckpointing sous la clé de Registre suivante.

**HKEY \_ local \_ machine \\ Software \\ Policies \\ Microsoft \\ Windows \\ installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 
