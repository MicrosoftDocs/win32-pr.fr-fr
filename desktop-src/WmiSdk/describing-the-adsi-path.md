---
description: Le protocole LDAP (Lightweight Directory Access Protocol) requiert que vous échappiez certains caractères avec une barre oblique inverse ( \) caractère quand vous les utilisez dans un chemin d’accès ADSI (Active Directory Service Interfaces) LDAP.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Description du chemin d’accès ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387108"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="985b0-103">Description du chemin d’accès ADSI</span><span class="sxs-lookup"><span data-stu-id="985b0-103">Describing the ADSI Path</span></span>

<span data-ttu-id="985b0-104">Le protocole LDAP (Lightweight Directory Access Protocol) requiert que vous échappiez certains caractères avec une barre oblique inverse ( \\ ) quand vous les utilisez dans un chemin d’accès ADSI (Active Directory Service Interfaces) LDAP.</span><span class="sxs-lookup"><span data-stu-id="985b0-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="985b0-105">, = +<>\# ; \\ »</span><span class="sxs-lookup"><span data-stu-id="985b0-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="985b0-106">Le caractère d’échappement est uniquement requis pour la valeur de la propriété **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="985b0-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="985b0-107">L’exemple suivant montre comment définir la propriété **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="985b0-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="985b0-108">Notez que le \# caractère de la valeur de propriété **CN** d’ABC \# est placé dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="985b0-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="985b0-109">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="985b0-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



