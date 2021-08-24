---
description: cette stratégie système par ordinateur désactive la création de points de contrôle par Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbea03dcab5db690f6fc06725dbb38a376310e967b9e92a9fcb0c59daab0180
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763509"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

cette [stratégie système](system-policy.md) par ordinateur désactive la création de points de contrôle par Windows Installer.

Si la valeur est 0 ou absente, le programme d’installation effectue un point de contrôle normal pour l’installation ou la désinstallation. Si la valeur est 1, le programme d’installation ne crée aucun point de contrôle.

cette stratégie affecte uniquement les points de contrôle définis par Windows Installer. sur les ordinateurs Windows XP, les administrateurs peuvent décider de désactiver les points de contrôle dans Windows Installer pour améliorer les performances. La [**restauration du système**](../sr/system-restore-portal.md) crée également des points de contrôle supplémentaires. pour plus d’informations, consultez [Points de restauration système et le Windows Installer](system-restore-points-and-the-windows-installer.md) et [définition d’un Point de restauration à partir d’une Action personnalisée](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Clé de Registre

Définissez la valeur nommée LimitSystemRestoreCheckpointing sous la clé de Registre suivante.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ policies \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

 

 
