---
title: IAgentCharacterEx GetHelpFileName
description: IAgentCharacterEx GetHelpFileName
ms.assetid: 52d5a874-ad3e-4833-9e3e-ff485414c54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d692de5704f88d14e32231a7d63fc80150f1481a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940165"
---
# <a name="iagentcharacterexgethelpfilename"></a><span data-ttu-id="5d8ce-103">IAgentCharacterEx::GetHelpFileName</span><span class="sxs-lookup"><span data-stu-id="5d8ce-103">IAgentCharacterEx::GetHelpFileName</span></span>

<span data-ttu-id="5d8ce-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d8ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpFileName(
   BSTR * pbszName  // address of Help filename
);
```

<span data-ttu-id="5d8ce-105">Récupère le HelpFileName d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-105">Retrieves the HelpFileName for a character.</span></span>

-   <span data-ttu-id="5d8ce-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5d8ce-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span><span class="sxs-lookup"><span data-stu-id="5d8ce-107"><span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*</span></span>
</dt> <dd>

<span data-ttu-id="5d8ce-108">Adresse d’une variable qui reçoit le nom de fichier d’aide pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-108">Address of a variable that receives the Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="5d8ce-109">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère ou sélectionne une commande dans son menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="5d8ce-110">S’il existe un numéro de contexte dans la propriété [**HelpContextID**](helpcontextid-property.md) de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».</span><span class="sxs-lookup"><span data-stu-id="5d8ce-110">If there is a context number in the selected command's [**HelpContextID**](helpcontextid-property.md) property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="5d8ce-111">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="5d8ce-112">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5d8ce-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5d8ce-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d8ce-113">See Also</span></span>

<span data-ttu-id="5d8ce-114">[**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="5d8ce-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




