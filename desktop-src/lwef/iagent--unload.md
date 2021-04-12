---
title: Déchargement IAgent
description: Déchargement IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315048"
---
# <a name="iagentunload"></a><span data-ttu-id="29912-103">IAgent :: Unload</span><span class="sxs-lookup"><span data-stu-id="29912-103">IAgent::UnLoad</span></span>

<span data-ttu-id="29912-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29912-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="29912-105">Décharge les données caractères pour le caractère spécifié à partir de la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="29912-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="29912-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="29912-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="29912-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="29912-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="29912-108">ID du caractère.</span><span class="sxs-lookup"><span data-stu-id="29912-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="29912-109">Utilisez cette méthode lorsque vous n’avez plus besoin d’un caractère, pour libérer de la mémoire utilisée pour stocker des informations sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="29912-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="29912-110">Si vous accédez de nouveau au caractère, utilisez la méthode [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="29912-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="29912-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29912-111">See Also</span></span>

[<span data-ttu-id="29912-112">**IAgent :: Load**</span><span class="sxs-lookup"><span data-stu-id="29912-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 