---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031158"
---
# <a name="iagentcommandsexgethelpcontextid"></a><span data-ttu-id="93e78-103">IAgentCommandsEx::GetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="93e78-103">IAgentCommandsEx::GetHelpContextID</span></span>

<span data-ttu-id="93e78-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93e78-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

<span data-ttu-id="93e78-105">Récupère le [**HelpContextID**](helpcontextid-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="93e78-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="93e78-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="93e78-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="93e78-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="93e78-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="93e78-108">Adresse d’une variable qui reçoit le numéro de contexte de la rubrique d’aide pour l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="93e78-108">Address of a variable that receives the context number of the help topic for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

<span data-ttu-id="93e78-109">Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne votre objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="93e78-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects your [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="93e78-110">S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="93e78-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="93e78-111">Le nombre de contextes actuels est la valeur de **HelpContextID** pour l’objet de **commande** .</span><span class="sxs-lookup"><span data-stu-id="93e78-111">The current context number is the value of **HelpContextID** for the **Command** object.</span></span>

<span data-ttu-id="93e78-112">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="93e78-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="93e78-113">La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="93e78-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="93e78-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93e78-114">See Also</span></span>

<span data-ttu-id="93e78-115">[**IAgentCommandsEx :: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="93e78-115">[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 