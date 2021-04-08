---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101561"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="5bd8a-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="5bd8a-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="5bd8a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5bd8a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="5bd8a-105">Définit la propriété [**Enabled**](enabled-property.md) pour la grammaire vocale des commandes globales de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="5bd8a-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5bd8a-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span><span class="sxs-lookup"><span data-stu-id="5bd8a-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="5bd8a-108">Valeur booléenne qui détermine si la grammaire vocale des commandes globales de l’agent est activée.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="5bd8a-109">**True** active la grammaire vocale ; **False** le désactive.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="5bd8a-110">Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="5bd8a-111">Lorsque la valeur est **false**, l’agent désactive tous les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets de [**commande**](/windows/desktop/lwef/the-command-object) du client.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="5bd8a-112">Cela vous permet de les éliminer de la grammaire active actuelle de votre client.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="5bd8a-113">Toutefois, étant donné que cela bloque potentiellement l’accès vocal à d’autres clients, réinitialisez cette propriété sur **true** après avoir traité l’entrée vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="5bd8a-114">La désactivation de la propriété n’affecte pas le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="5bd8a-115">Les commandes globales ajoutées par le serveur s’affichent toujours.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="5bd8a-116">Vous ne pouvez pas les supprimer du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bd8a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bd8a-117">See Also</span></span>

[<span data-ttu-id="5bd8a-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5bd8a-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 