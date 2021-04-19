---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538792"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="03e43-103">IAgentCharacter :: SetName</span><span class="sxs-lookup"><span data-stu-id="03e43-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="03e43-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03e43-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="03e43-105">Définit le nom du caractère.</span><span class="sxs-lookup"><span data-stu-id="03e43-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="03e43-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="03e43-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="03e43-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="03e43-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="03e43-108">BSTR qui définit le nom du caractère.</span><span class="sxs-lookup"><span data-stu-id="03e43-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="03e43-109">Le nom par défaut d’un caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="03e43-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="03e43-110">Vous pouvez le modifier à l’aide de **IAgentCharacter :: SetName**; Toutefois, cela modifie le nom de caractère pour tous les clients actuels du caractère.</span><span class="sxs-lookup"><span data-stu-id="03e43-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="03e43-111">Cette propriété n’est pas persistante (stockée définitivement).</span><span class="sxs-lookup"><span data-stu-id="03e43-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="03e43-112">Le nom du caractère revient à son nom par défaut chaque fois que le caractère est chargé pour la première fois par un client.</span><span class="sxs-lookup"><span data-stu-id="03e43-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="03e43-113">Le nom du caractère peut également dépendre de son ID de langue.</span><span class="sxs-lookup"><span data-stu-id="03e43-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="03e43-114">Les caractères peuvent être compilés avec des noms différents dans différentes langues.</span><span class="sxs-lookup"><span data-stu-id="03e43-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="03e43-115">Le serveur utilise le paramètre de nom du caractère dans des parties de l’interface de l’agent Microsoft, telles que le titre de la fenêtre commandes vocales lorsque le caractère est en entrée-actif et dans le menu contextuel de la barre des tâches de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03e43-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="03e43-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03e43-116">See Also</span></span>

[<span data-ttu-id="03e43-117">**IAgentCharacter :: GetName**</span><span class="sxs-lookup"><span data-stu-id="03e43-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




