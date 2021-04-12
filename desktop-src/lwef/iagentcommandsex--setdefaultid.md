---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381858"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="56518-103">IAgentCommandsEx::SetDefaultID</span><span class="sxs-lookup"><span data-stu-id="56518-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="56518-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56518-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="56518-105">Définit l’ID de la commande par défaut dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="56518-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="56518-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="56518-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="56518-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="56518-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="56518-108">ID de la [**commande**](/windows/desktop/lwef/the-command-object) à définir comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="56518-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="56518-109">Cette propriété définit le jeu d’objets de [**commande**](/windows/desktop/lwef/the-command-object) par défaut dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="56518-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="56518-110">La commande par défaut est en gras dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="56518-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="56518-111">Toutefois, la définition de la commande par défaut ne modifie pas réellement les événements de gestion des commandes ou de double-clic.</span><span class="sxs-lookup"><span data-stu-id="56518-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="56518-112">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="56518-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="56518-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56518-113">See Also</span></span>

[<span data-ttu-id="56518-114">**IAgentCommandsEx::GetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="56518-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 