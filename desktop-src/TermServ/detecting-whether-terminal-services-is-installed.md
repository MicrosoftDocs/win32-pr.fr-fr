---
title: Détection de l’installation du rôle Services Bureau à distance
description: exemple de code C \ qui affiche une méthode qui retourne la valeur True si le rôle serveur Services Bureau à distance est installé et en cours d’exécution ou false dans le cas contraire, en commençant par Windows server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871759"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Détection de l’installation du rôle Services Bureau à distance

Vous pouvez utiliser la classe WMI [**\_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI pour détecter si le rôle serveur services Bureau à distance est installé.

L’exemple C# suivant présente une méthode qui retourne la **valeur true** si le rôle serveur services Bureau à distance est installé et en cours d’exécution ou **false** dans le cas contraire. étant donné que la classe WMI [**Win32 \_ ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) est disponible uniquement à partir de Windows Server 2008, ce code n’est pas compatible avec les versions antérieures de Windows.


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



 

 