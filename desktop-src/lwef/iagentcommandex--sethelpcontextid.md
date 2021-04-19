---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106518007"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="030df-103">IAgentCommandEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="030df-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="030df-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="030df-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="030df-105">Définit la [**HelpContextID**](helpcontextid-property-com.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="030df-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="030df-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="030df-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="030df-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span><span class="sxs-lookup"><span data-stu-id="030df-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="030df-108">Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.</span><span class="sxs-lookup"><span data-stu-id="030df-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="030df-109">Si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère.</span><span class="sxs-lookup"><span data-stu-id="030df-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="030df-110">Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande.</span><span class="sxs-lookup"><span data-stu-id="030df-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="030df-111">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property-com.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="030df-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="030df-112">Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.</span><span class="sxs-lookup"><span data-stu-id="030df-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="030df-113">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="030df-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="030df-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="030df-114">See Also</span></span>

<span data-ttu-id="030df-115">[**IAgentCommandEx :: GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="030df-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 