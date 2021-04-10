---
title: IAgentCharacterEx SetHelpFileName
description: IAgentCharacterEx SetHelpFileName
ms.assetid: 1f8d2bd7-5821-46c0-b371-7ecbc526df72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1342baecc1e059d4fcb5d1323c0c714bd6bf7087
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100712"
---
# <a name="iagentcharacterexsethelpfilename"></a><span data-ttu-id="a78fa-103">IAgentCharacterEx::SetHelpFileName</span><span class="sxs-lookup"><span data-stu-id="a78fa-103">IAgentCharacterEx::SetHelpFileName</span></span>

<span data-ttu-id="a78fa-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a78fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpFileName(
   BSTR bszName  // Help filename
);
```

<span data-ttu-id="a78fa-105">Définit le HelpFileName d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="a78fa-105">Sets the HelpFileName for a character.</span></span>

-   <span data-ttu-id="a78fa-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a78fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a78fa-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="a78fa-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="a78fa-108">Nom du fichier d’aide pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="a78fa-108">The Help filename for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a78fa-109">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur clique sur le caractère ou sélectionne une commande dans son menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="a78fa-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="a78fa-110">S’il existe un numéro de contexte dans la propriété [**HelpContextID**](helpcontextid-property.md) de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».</span><span class="sxs-lookup"><span data-stu-id="a78fa-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="a78fa-111">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="a78fa-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="a78fa-112">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a78fa-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="a78fa-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a78fa-113">See Also</span></span>

<span data-ttu-id="a78fa-114">[**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="a78fa-114">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::GetHelpFileName**](iagentcharacterex--gethelpfilename.md)</span></span>


 

 




