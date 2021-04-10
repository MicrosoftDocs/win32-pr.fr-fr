---
description: Les actions personnalisées ne doivent pas appeler la fonction SRSetRestorePoint, car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Définition d’un point de restauration à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115826"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a><span data-ttu-id="1cb46-103">Définition d’un point de restauration à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="1cb46-103">Setting a Restore Point from a Custom Action</span></span>

<span data-ttu-id="1cb46-104">Les actions personnalisées ne doivent pas appeler la fonction [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1cb46-104">Custom actions must not call the [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) function because this may result in a restore entry point being written into the middle of a Windows Installer installation.</span></span>

<span data-ttu-id="1cb46-105">Pour plus d’informations, consultez [points de restauration du système et le Windows Installer](system-restore-points-and-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="1cb46-105">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md).</span></span>

 

 
