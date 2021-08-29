---
description: dans Windows 7, WMI implémentait la \_ classe Win32 OptionalFeature. Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Interrogation de l’état des fonctionnalités facultatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a8cceccdfeec6f902a56e8903a1d41e504750e
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786685"
---
# <a name="querying-the-status-of-optional-features"></a>Interrogation de l’état des fonctionnalités facultatives

dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.

vous pouvez utiliser Windows PowerShell applets de commande pour interroger l’état des fonctionnalités facultatives. Tous les exemples de cette rubrique utilisent l’applet de commande Get-WmiObject. Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Pour récupérer toutes les instances de fonctionnalités facultatives présentes sur un ordinateur**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Pour rechercher une fonctionnalité facultative en spécifiant le nom de la fonctionnalité**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Pour rechercher des fonctionnalités facultatives en spécifiant l’état d’installation**


    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_OptionalFeature Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
