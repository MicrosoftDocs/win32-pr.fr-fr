---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381933"
---
# <a name="iagentcommandexgethelpcontextid"></a><span data-ttu-id="2f7e3-103">IAgentCommandEx::GetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="2f7e3-103">IAgentCommandEx::GetHelpContextID</span></span>

<span data-ttu-id="2f7e3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f7e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

<span data-ttu-id="2f7e3-105">Récupère le [**HelpContextID**](helpcontextid-property-com.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2f7e3-105">Retrieves the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="2f7e3-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2f7e3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2f7e3-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span><span class="sxs-lookup"><span data-stu-id="2f7e3-107"><span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*</span></span>
</dt> <dd>

<span data-ttu-id="2f7e3-108">Adresse d’une variable qui reçoit le numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="2f7e3-108">Address of a variable that receives the context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="2f7e3-109">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) de votre caractère sur ce fichier, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande.</span><span class="sxs-lookup"><span data-stu-id="2f7e3-109">If you've created a Windows Help file for your application and set your character's [**HelpFile**](helpfile-property.md) property to this file, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="2f7e3-110">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property-com.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="2f7e3-110">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="2f7e3-111">Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.</span><span class="sxs-lookup"><span data-stu-id="2f7e3-111">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="2f7e3-112">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2f7e3-112">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="2f7e3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f7e3-113">See Also</span></span>

<span data-ttu-id="2f7e3-114">[**IAgentCommandEx :: SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="2f7e3-114">[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 