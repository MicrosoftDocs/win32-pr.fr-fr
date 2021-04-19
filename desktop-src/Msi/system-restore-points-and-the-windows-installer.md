---
description: La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur. Pour plus d’informations, consultez restauration du système.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Points de restauration système et Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516947"
---
# <a name="system-restore-points-and-the-windows-installer"></a><span data-ttu-id="fe066-104">Points de restauration système et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fe066-104">System Restore Points and the Windows Installer</span></span>

<span data-ttu-id="fe066-105">La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fe066-105">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="fe066-106">Pour plus d’informations, consultez [restauration du système](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fe066-106">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="fe066-107">Les points de restauration système sont créés par le système et sont également créés par Windows Installer lors de l’installation ou de la suppression d’un logiciel.</span><span class="sxs-lookup"><span data-stu-id="fe066-107">System restore points are created by the system and are also created by Windows Installer when software is installed or removed.</span></span>

<span data-ttu-id="fe066-108">Sur Windows XP, le programme d’installation peut créer des points de contrôle lors de la première installation d’une application et Pendant sa suppression.</span><span class="sxs-lookup"><span data-stu-id="fe066-108">On Windows XP, the installer may create checkpoints during the first installation of an application, and during its removal.</span></span> <span data-ttu-id="fe066-109">Le programme d’installation crée uniquement des points de contrôle dans ce cas lorsque la modification est exécutée avec au moins une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fe066-109">The installer only creates checkpoints in these cases when the change is run with at least a [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="fe066-110">Les installations dont le [niveau d’interface utilisateur](user-interface-levels.md) est défini sur aucun sont généralement initiées par le système ou par une application qui doit gérer la création d’un point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe066-110">Installations having the [user interface level](user-interface-levels.md) set to None are usually initiated by the system or an application that should handle creating a checkpoint.</span></span> <span data-ttu-id="fe066-111">Pour plus d’informations, consultez [restauration du système](../sr/system-restore-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fe066-111">For more information, see [System Restore](../sr/system-restore-portal.md).</span></span>

<span data-ttu-id="fe066-112">Dans les entreprises avec de nombreuses petites applications, les administrateurs peuvent décider de désactiver les points de contrôle dans le programme d’installation pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="fe066-112">In corporations with many small applications, administrators may decide to disable checkpointing from within the installer to improve performance.</span></span> <span data-ttu-id="fe066-113">Pour plus d’informations, consultez [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) ou [définition d’un point de restauration à partir d’une action personnalisée](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="fe066-113">For more information, see [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) or [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

<span data-ttu-id="fe066-114">À partir de Windows Installer 5,0, la propriété [**MSIFASTINSTALL**](msifastinstall.md) peut être définie pour empêcher une installation de générer un point de restauration système.</span><span class="sxs-lookup"><span data-stu-id="fe066-114">Beginning with Windows Installer 5.0, the [**MSIFASTINSTALL**](msifastinstall.md) property can be set to prevent an installation from generating a system restore point.</span></span>

 

 
