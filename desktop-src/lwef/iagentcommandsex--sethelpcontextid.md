---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725924"
---
# <a name="iagentcommandsexsethelpcontextid"></a><span data-ttu-id="27c0f-103">IAgentCommandsEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="27c0f-103">IAgentCommandsEx::SetHelpContextID</span></span>

<span data-ttu-id="27c0f-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27c0f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="27c0f-105">Définit la [**HelpContextID**](helpcontextid-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="27c0f-105">Sets the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="27c0f-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="27c0f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="27c0f-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="27c0f-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="27c0f-108">Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.</span><span class="sxs-lookup"><span data-stu-id="27c0f-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="27c0f-109">Si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère.</span><span class="sxs-lookup"><span data-stu-id="27c0f-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="27c0f-110">L’agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande.</span><span class="sxs-lookup"><span data-stu-id="27c0f-110">Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="27c0f-111">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="27c0f-111">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="27c0f-112">Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.</span><span class="sxs-lookup"><span data-stu-id="27c0f-112">The current context number is the value of **HelpContextID** for the command.</span></span> <span data-ttu-id="27c0f-113">S’il existe un numéro de contexte dans la propriété **HelpContextID** de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».</span><span class="sxs-lookup"><span data-stu-id="27c0f-113">If there is a context number in the selected command's **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="27c0f-114">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="27c0f-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="27c0f-115">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="27c0f-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="27c0f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27c0f-116">See Also</span></span>

<span data-ttu-id="27c0f-117">[**IAgentCommandsEx :: GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="27c0f-117">[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 