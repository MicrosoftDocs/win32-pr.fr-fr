---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672174"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="4ad9a-103">IAgentCharacterEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="4ad9a-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="4ad9a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ad9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="4ad9a-105">Définit la [**HelpContextID**](helpcontextid-property.md) pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="4ad9a-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4ad9a-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="4ad9a-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="4ad9a-108">Le numéro de contexte de la rubrique d’aide associée à un caractère ; utilisé pour fournir une aide contextuelle pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="4ad9a-109">Si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne le caractère.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="4ad9a-110">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="4ad9a-111">Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="4ad9a-112">S’il existe un numéro de contexte dans la propriété **HelpContextID** , help affiche une rubrique correspondant au contexte d’aide actuel ; Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».</span><span class="sxs-lookup"><span data-stu-id="4ad9a-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="4ad9a-113">Ce paramètre s’applique uniquement lorsque votre application cliente est le client actif du premier caractère.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="4ad9a-114">Elle n’affecte pas les autres clients du caractère ou d’autres caractères que votre application cliente utilise.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="4ad9a-115">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4ad9a-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4ad9a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ad9a-116">See Also</span></span>

<span data-ttu-id="4ad9a-117">[**IAgentCharacterEx :: GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="4ad9a-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




