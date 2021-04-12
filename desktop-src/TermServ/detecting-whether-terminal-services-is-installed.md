---
title: Détection de l’installation du rôle Services Bureau à distance
description: Exemple de code C \ qui affiche une méthode qui retourne la valeur true si le rôle serveur Services Bureau à distance est installé et en cours d’exécution ou false dans le cas contraire, à compter de Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382428"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a><span data-ttu-id="e166f-103">Détection de l’installation du rôle Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="e166f-103">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>

<span data-ttu-id="e166f-104">Vous pouvez utiliser la classe WMI [**\_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI pour détecter si le rôle serveur services Bureau à distance est installé.</span><span class="sxs-lookup"><span data-stu-id="e166f-104">You can use the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class to detect whether the Remote Desktop Services server role is installed.</span></span>

<span data-ttu-id="e166f-105">L’exemple C# suivant présente une méthode qui retourne la **valeur true** si le rôle serveur services Bureau à distance est installé et en cours d’exécution ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e166f-105">The following C# example shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise.</span></span> <span data-ttu-id="e166f-106">Étant donné que la classe WMI [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) est disponible uniquement à partir de Windows Server 2008, ce code n’est pas compatible avec les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="e166f-106">Because the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class is only available beginning with Windows Server 2008, this code is not compatible with earlier versions of Windows.</span></span>


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 