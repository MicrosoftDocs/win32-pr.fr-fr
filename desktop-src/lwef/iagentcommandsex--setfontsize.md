---
title: IAgentCommandsEx SetFontSize
description: IAgentCommandsEx SetFontSize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463015"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="7731b-103">IAgentCommandsEx::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="7731b-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="7731b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7731b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="7731b-105">Définit la taille de la police affichée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="7731b-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="7731b-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7731b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7731b-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="7731b-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="7731b-108">Taille de la police.</span><span class="sxs-lookup"><span data-stu-id="7731b-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="7731b-109">Cette propriété détermine la taille en points de la police utilisée pour afficher le texte dans le menu contextuel du caractère quand votre application cliente est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="7731b-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="7731b-110">La valeur par défaut du paramètre font est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère, ou si ce n’est pas le cas, il s’agit du paramètre de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7731b-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="7731b-111">S’il n’est pas en entrée-actif, le texte de la [**légende**](caption-property.md) de [**commande**](/windows/desktop/lwef/the-command-object) de votre application cliente apparaît dans la taille en points spécifiée pour le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="7731b-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="7731b-112">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="7731b-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="7731b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7731b-113">See Also</span></span>

<span data-ttu-id="7731b-114">[**IAgentCommandsEx :: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx :: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="7731b-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 