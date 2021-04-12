---
description: Le protocole LDAP (Lightweight Directory Access Protocol) requiert que vous échappiez certains caractères avec une barre oblique inverse ( \) caractère quand vous les utilisez dans un chemin d’accès ADSI (Active Directory Service Interfaces) LDAP.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Description du chemin d’accès ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528611"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="dd170-103">Description du chemin d’accès ADSI</span><span class="sxs-lookup"><span data-stu-id="dd170-103">Describing the ADSI Path</span></span>

<span data-ttu-id="dd170-104">Le protocole LDAP (Lightweight Directory Access Protocol) requiert que vous échappiez certains caractères avec une barre oblique inverse ( \) caractère quand vous les utilisez dans un chemin d’accès ADSI (Active Directory Service Interfaces) LDAP.</span><span class="sxs-lookup"><span data-stu-id="dd170-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="dd170-105">, = +<>\# ; \\ »</span><span class="sxs-lookup"><span data-stu-id="dd170-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="dd170-106">Le caractère d’échappement est uniquement requis pour la valeur de la propriété **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="dd170-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="dd170-107">L’exemple suivant montre comment définir la propriété **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="dd170-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="dd170-108">Notez que le \# caractère de la valeur de propriété **CN** d’ABC \# est placé dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="dd170-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> <span data-ttu-id="dd170-109">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="dd170-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



