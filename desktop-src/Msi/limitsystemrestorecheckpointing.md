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
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="b31dc-103">LimitSystemRestoreCheckpointing</span><span class="sxs-lookup"><span data-stu-id="b31dc-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="b31dc-104">Cette [stratégie système](system-policy.md) par ordinateur désactive la création de points de contrôle par Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b31dc-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="b31dc-105">Si la valeur est 0 ou absente, le programme d’installation effectue un point de contrôle normal pour l’installation ou la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="b31dc-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="b31dc-106">Si la valeur est 1, le programme d’installation ne crée aucun point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b31dc-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="b31dc-107">Cette stratégie affecte uniquement les points de contrôle définis par Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b31dc-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="b31dc-108">Sur les ordinateurs Windows XP, les administrateurs peuvent décider de désactiver les points de contrôle à partir de Windows Installer pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="b31dc-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="b31dc-109">La [**restauration du système**](../sr/system-restore-portal.md) crée également des points de contrôle supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b31dc-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="b31dc-110">Pour plus d’informations, consultez [points de restauration système et le Windows Installer](system-restore-points-and-the-windows-installer.md) et [définition d’un point de restauration à partir d’une action personnalisée](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="b31dc-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="b31dc-111">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="b31dc-111">Registry Key</span></span>

<span data-ttu-id="b31dc-112">Définissez la valeur nommée LimitSystemRestoreCheckpointing sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="b31dc-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="b31dc-113">**HKEY \_ local \_ machine \\ Software \\ Policies \\ Microsoft \\ Windows \\ installer**</span><span class="sxs-lookup"><span data-stu-id="b31dc-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="b31dc-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="b31dc-114">Data Type</span></span>

<span data-ttu-id="b31dc-115">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="b31dc-115">**REG\_DWORD**</span></span>

 

 
