---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381955"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="f44cb-103">IAgentCommandsEx::GetDefaultID</span><span class="sxs-lookup"><span data-stu-id="f44cb-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="f44cb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f44cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="f44cb-105">Récupère l’ID de la commande par défaut dans une collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f44cb-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="f44cb-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f44cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f44cb-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="f44cb-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="f44cb-108">Adresse d’une variable qui reçoit l’ID de la [**commande**](/windows/desktop/lwef/the-command-object) définie comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f44cb-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="f44cb-109">Cette propriété retourne l’objet de [**commande**](/windows/desktop/lwef/the-command-object) par défaut actuel dans votre collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f44cb-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="f44cb-110">La commande par défaut est en gras dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="f44cb-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="f44cb-111">Toutefois, la définition de la commande par défaut ne modifie pas les événements de gestion des commandes ou de double-clic.</span><span class="sxs-lookup"><span data-stu-id="f44cb-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="f44cb-112">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="f44cb-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="f44cb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f44cb-113">See Also</span></span>

[<span data-ttu-id="f44cb-114">**IAgentCommandsEx::SetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="f44cb-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 