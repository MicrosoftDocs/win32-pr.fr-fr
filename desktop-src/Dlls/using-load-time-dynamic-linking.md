---
description: Une fois que vous avez créé une DLL, vous pouvez utiliser les fonctions qu’elle définit dans une application. Voici une application console simple qui utilise la fonction myPuts exportée à partir de Myputs.dll (consultez Création d’une bibliothèque de Dynamic-Link simple).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Utilisation de la liaison dynamique Load-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521498"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="81dc0-104">Utilisation de la liaison dynamique Load-Time</span><span class="sxs-lookup"><span data-stu-id="81dc0-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="81dc0-105">Une fois que vous avez créé une DLL, vous pouvez utiliser les fonctions qu’elle définit dans une application.</span><span class="sxs-lookup"><span data-stu-id="81dc0-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="81dc0-106">Voici une application console simple qui utilise la fonction myPuts exportée à partir de Myputs.dll (consultez [création d’une bibliothèque de Dynamic-Link simple](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="81dc0-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="81dc0-107">Étant donné que cet exemple appelle la fonction DLL explicitement, le module de l’application doit être lié à la bibliothèque d’importation Myputs. lib.</span><span class="sxs-lookup"><span data-stu-id="81dc0-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="81dc0-108">Pour plus d’informations sur la création de dll, consultez la documentation fournie avec vos outils de développement.</span><span class="sxs-lookup"><span data-stu-id="81dc0-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="81dc0-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81dc0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81dc0-110">Liaison dynamique au moment du chargement</span><span class="sxs-lookup"><span data-stu-id="81dc0-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



