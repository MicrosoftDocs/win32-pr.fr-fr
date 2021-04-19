---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511484"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="36aab-103">IAgentCommands :: SetVisible</span><span class="sxs-lookup"><span data-stu-id="36aab-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="36aab-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36aab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="36aab-105">Définit la valeur de la propriété [**visible**](visible-property.md) pour une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="36aab-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="36aab-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="36aab-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="36aab-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="36aab-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="36aab-108">Valeur booléenne qui détermine la propriété [**visible**](visible-property.md) d’une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="36aab-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="36aab-109">**True** définit la [**légende**](caption-property.md) de la collection **Commands** pour qu’elle soit visible lorsque le menu contextuel du caractère s’affiche ; *False* ne l’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="36aab-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="36aab-110">Une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) doit avoir sa propriété [**Caption**](caption-property.md) définie et sa propriété [**visible**](visible-property.md) définie sur **true** pour apparaître dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="36aab-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="36aab-111">La propriété **visible** doit également avoir la valeur **true** pour que les commandes de la collection s’affichent lorsque votre application cliente est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="36aab-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="36aab-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36aab-112">See Also</span></span>

<span data-ttu-id="36aab-113">[**IAgentCommands :: getVisible**](iagentcommands--getvisible.md), [ **IAgentCommand :: SetCaption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="36aab-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 