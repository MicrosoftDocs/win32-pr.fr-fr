---
description: Une action personnalisée peut appeler une fonction définie dans une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Bibliothèques de Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034643"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="06c05-103">Bibliothèques de Dynamic-Link (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="06c05-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="06c05-104">Une action personnalisée peut appeler une fonction définie dans une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="06c05-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="06c05-105">La DLL peut exister en tant que fichier installé pendant l’installation actuelle ou en tant que flux binaire temporaire provenant de la [table binaire](binary-table.md) de la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="06c05-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="06c05-106">Notez que toutes les fonctions appelées, y compris les actions personnalisées dans les dll, doivent spécifier la \_ \_ Convention d’appel StdCall.</span><span class="sxs-lookup"><span data-stu-id="06c05-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="06c05-107">Par exemple, pour appeler CustomAction, utilisez ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="06c05-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="06c05-108">Pour plus d’informations, consultez [accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span><span class="sxs-lookup"><span data-stu-id="06c05-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="06c05-109">Les types d’actions personnalisées suivants appellent une bibliothèque de liens dynamiques.</span><span class="sxs-lookup"><span data-stu-id="06c05-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="06c05-110">Type d’action personnalisé</span><span class="sxs-lookup"><span data-stu-id="06c05-110">Custom action type</span></span>                                 | <span data-ttu-id="06c05-111">Description</span><span class="sxs-lookup"><span data-stu-id="06c05-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="06c05-112">Type d’action personnalisé 1</span><span class="sxs-lookup"><span data-stu-id="06c05-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="06c05-113">Fichier DLL stocké dans un flux de table binaire.</span><span class="sxs-lookup"><span data-stu-id="06c05-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="06c05-114">Type d’action personnalisée 17</span><span class="sxs-lookup"><span data-stu-id="06c05-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="06c05-115">Fichier DLL installé avec un produit.</span><span class="sxs-lookup"><span data-stu-id="06c05-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="06c05-116">Pour utiliser COM, vous devez appeler [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) dans l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="06c05-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="06c05-117">Ne quittez pas si vous constatez que le thread a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="06c05-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="06c05-118">Par exemple, le thread est initialisé dans une installation par ordinateur, mais pas dans une installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06c05-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="06c05-119">Consultez la [liste récapitulative de tous les types d’actions personnalisées](summary-list-of-all-custom-action-types.md) pour obtenir un résumé de tous les types d’actions personnalisées et la façon dont elles sont encodées dans la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="06c05-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
