---
description: dans Windows 7, WMI implémentait la \_ classe Win32 OptionalFeature. Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Interrogation de l’état des fonctionnalités facultatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecffe6ddbe9b860c6f49fe12d3fed500c169bef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476705"
---
# <a name="querying-the-status-of-optional-features"></a>Interrogation de l’état des fonctionnalités facultatives

dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.

vous pouvez utiliser Windows PowerShell applets de commande pour interroger l’état des fonctionnalités facultatives. Tous les exemples de cette rubrique utilisent l’applet de commande Get-WmiObject. Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Pour récupérer toutes les instances de fonctionnalités facultatives présentes sur un ordinateur**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject Win32_OptionalFeature</code></pre> | 


    

**Pour rechercher une fonctionnalité facultative en spécifiant le nom de la fonctionnalité**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from Win32_OptionalFeature where name = 'TelnetClient'"</code></pre> | 


    

    > [!Note]  
    > The **name** property is case-sensitive.

     

**Pour rechercher des fonctionnalités facultatives en spécifiant l’état d’installation**

-   <span codelanguage="PowerShell"></span>
    
| PowerShell | 
|------------|
| <pre><code>Get-WmiObject -query "select * from win32_optionalfeature where installstate= 1"</code></pre> | 


    

    For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_OptionalFeature Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
