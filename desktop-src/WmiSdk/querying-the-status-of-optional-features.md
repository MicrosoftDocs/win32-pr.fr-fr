---
description: dans Windows 7, WMI implémentait la \_ classe Win32 OptionalFeature. Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Interrogation de l’état des fonctionnalités facultatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec27457336adcc5c358aad0a5e139c1c7c07f6bcb72335ec549f9ca98cc1e5a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996029"
---
# <a name="querying-the-status-of-optional-features"></a>Interrogation de l’état des fonctionnalités facultatives

dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.

vous pouvez utiliser Windows PowerShell applets de commande pour interroger l’état des fonctionnalités facultatives. Tous les exemples de cette rubrique utilisent l’applet de commande Get-WmiObject. Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).

**Pour récupérer toutes les instances de fonctionnalités facultatives présentes sur un ordinateur**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

**Pour rechercher une fonctionnalité facultative en spécifiant le nom de la fonctionnalité**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > La propriété **Name** respecte la casse.

     

**Pour rechercher des fonctionnalités facultatives en spécifiant l’état d’installation**

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>PowerShell</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    Pour plus d’informations sur les valeurs possibles de la propriété **InstallState** , consultez [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_OptionalFeature Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
