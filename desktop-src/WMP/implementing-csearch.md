---
title: Implémentation de CSearch
description: Implémentation de CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-ins du lecteur Windows Media, classe CSearch
- plug-ins, classe CSearch
- plug-ins d’interface utilisateur, classe CSearch
- Plug-ins d’interface utilisateur, classe CSearch
- CSearch, classe
- Guide de programmation, plug-ins d’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507131"
---
# <a name="implementing-csearch"></a><span data-ttu-id="8c46f-109">Implémentation de CSearch</span><span class="sxs-lookup"><span data-stu-id="8c46f-109">Implementing CSearch</span></span>

<span data-ttu-id="8c46f-110">L’interface **IWMPPluginUI** possède plusieurs méthodes qui sont appelées par le lecteur Windows Media à des moments différents pendant le cycle de vie d’une instance de plug-in.</span><span class="sxs-lookup"><span data-stu-id="8c46f-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="8c46f-111">L’Assistant fournit des implémentations de base de ces méthodes, ainsi que le constructeur de classe et le destructeur, ainsi que d’autres méthodes de classe.</span><span class="sxs-lookup"><span data-stu-id="8c46f-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="8c46f-112">Le fichier Search. h doit être modifié de sorte que le lecteur Windows Media puisse communiquer avec l’interface utilisateur, ce qui est décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="8c46f-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="8c46f-113">Pour que la classe CPluginWindow ait accès à la variable de membre privé m \_ Core, une déclaration de classe Friend doit être effectuée à l’intérieur de la définition de la classe CSearch, comme indiqué dans l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="8c46f-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="8c46f-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c46f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c46f-115">**Guide de programmation de plug-ins d’interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8c46f-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




