---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381877"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="a75e4-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="a75e4-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="a75e4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a75e4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="a75e4-105">Récupère si la grammaire vocale pour les commandes globales de l’agent est activée.</span><span class="sxs-lookup"><span data-stu-id="a75e4-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="a75e4-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a75e4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a75e4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="a75e4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="a75e4-108">Adresse qui reçoit la **valeur true** si la grammaire vocale pour les commandes globales de l’agent est activée, **false** si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a75e4-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="a75e4-109">Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère.</span><span class="sxs-lookup"><span data-stu-id="a75e4-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="a75e4-110">Lorsque cette méthode retourne la **valeur false**, les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets de [**commande**](/windows/desktop/lwef/the-command-object) d’autres clients, ne sont pas inclus dans la grammaire.</span><span class="sxs-lookup"><span data-stu-id="a75e4-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="a75e4-111">Cela vous permet de les éliminer de la grammaire active actuelle de votre client.</span><span class="sxs-lookup"><span data-stu-id="a75e4-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="a75e4-112">Toutefois, ce paramètre ne reflète pas l’inclusion de ces commandes dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="a75e4-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="a75e4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a75e4-113">See Also</span></span>

[<span data-ttu-id="a75e4-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a75e4-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 