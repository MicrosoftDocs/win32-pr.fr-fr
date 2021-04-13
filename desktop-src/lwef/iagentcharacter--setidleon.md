---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380438"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="bbf32-103">IAgentCharacter::SetIdleOn</span><span class="sxs-lookup"><span data-stu-id="bbf32-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="bbf32-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bbf32-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="bbf32-105">Définit le traitement d’inactivité automatique d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="bbf32-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="bbf32-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="bbf32-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bbf32-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Ble*</span><span class="sxs-lookup"><span data-stu-id="bbf32-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="bbf32-108">Indicateur de traitement inactif.</span><span class="sxs-lookup"><span data-stu-id="bbf32-108">Idle processing flag.</span></span> <span data-ttu-id="bbf32-109">Si ce paramètre a la **valeur true**, l’agent Microsoft lit automatiquement les animations d’état **ralenti** .</span><span class="sxs-lookup"><span data-stu-id="bbf32-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="bbf32-110">Le serveur définit automatiquement un délai d’attente après la dernière animation d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="bbf32-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="bbf32-111">Lorsque l’intervalle de ce minuteur est terminé, le serveur commence les États de **ralenti** pour un caractère, en lisant ses animations de **ralenti** associées à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="bbf32-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="bbf32-112">Si vous souhaitez gérer vous-même les animations d’état **ralenti** , affectez la valeur **false** à la propriété.</span><span class="sxs-lookup"><span data-stu-id="bbf32-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="bbf32-113">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="bbf32-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbf32-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf32-114">See Also</span></span>

[<span data-ttu-id="bbf32-115">**IAgentCharacter::GetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="bbf32-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




