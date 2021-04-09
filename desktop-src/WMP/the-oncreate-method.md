---
title: La méthode OnCreate
description: La méthode OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Plug-ins du lecteur Windows Media, méthode OnCreate
- plug-ins, méthode OnCreate
- plug-ins d’interface utilisateur, méthode OnCreate
- Plug-ins d’interface utilisateur, méthode OnCreate
- OnCreate, méthode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839394"
---
# <a name="the-oncreate-method"></a><span data-ttu-id="32b61-108">La méthode OnCreate</span><span class="sxs-lookup"><span data-stu-id="32b61-108">The OnCreate Method</span></span>

<span data-ttu-id="32b61-109">La méthode OnCreate est appelée lors de la création initiale de la fenêtre de plug-in.</span><span class="sxs-lookup"><span data-stu-id="32b61-109">The OnCreate method is called when the plug-in window is first created.</span></span>

<span data-ttu-id="32b61-110">Le code suivant est utilisé pour implémenter cette méthode :</span><span class="sxs-lookup"><span data-stu-id="32b61-110">The following code is used to implement this method:</span></span>


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



<span data-ttu-id="32b61-111">Cette méthode crée le bouton de **recherche** et l’associe à l' \_ ID de commande de recherche IDC, qui est défini au début du fichier :</span><span class="sxs-lookup"><span data-stu-id="32b61-111">This method creates the **Search** button and associates it with the IDC\_SEARCH command ID, which is defined at the beginning of the file:</span></span>


```C++
#define IDC_SEARCH 2000

```



<span data-ttu-id="32b61-112">Cet ID de commande est mappé à la méthode OnSearch dans la section de la table des messages décrite précédemment.</span><span class="sxs-lookup"><span data-stu-id="32b61-112">This command ID is mapped to the OnSearch method in the message map section described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32b61-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="32b61-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b61-114">**Implémentation de CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="32b61-114">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




