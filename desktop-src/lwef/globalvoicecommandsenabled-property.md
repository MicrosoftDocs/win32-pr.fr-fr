---
title: Propriété GlobalVoiceCommandsEnabled
description: Propriété GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103941001"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="dc44c-103">Propriété GlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="dc44c-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="dc44c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc44c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dc44c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="dc44c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dc44c-106">Retourne ou définit si la voix est activée pour les commandes globales de l’agent.</span><span class="sxs-lookup"><span data-stu-id="dc44c-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="dc44c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="dc44c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dc44c-108">*agent. ***Caractères («*** CharacterID \* \* * »). Commands. GlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="dc44c-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="dc44c-109">\[ = *expression*\]</span><span class="sxs-lookup"><span data-stu-id="dc44c-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="dc44c-110">Partie</span><span class="sxs-lookup"><span data-stu-id="dc44c-110">Part</span></span>      | <span data-ttu-id="dc44c-111">Description</span><span class="sxs-lookup"><span data-stu-id="dc44c-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc44c-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="dc44c-112">*boolean*</span></span> | <span data-ttu-id="dc44c-113">Expression booléenne qui indique si les paramètres vocaux pour les commandes globales de l’agent sont activés.</span><span class="sxs-lookup"><span data-stu-id="dc44c-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="dc44c-114">**True** (par défaut) les paramètres vocaux sont activés.</span><span class="sxs-lookup"><span data-stu-id="dc44c-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="dc44c-115">**Valeur false** Les paramètres vocaux sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="dc44c-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc44c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="dc44c-116">Remarks</span></span>

<span data-ttu-id="dc44c-117">Microsoft Agent ajoute automatiquement des paramètres vocaux (grammaire) pour l’ouverture et la fermeture de la fenêtre commandes vocales et pour l’affichage et le masquage du caractère.</span><span class="sxs-lookup"><span data-stu-id="dc44c-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="dc44c-118">Si vous affectez à **GlobalVoiceCommandsEnabled** la **valeur false**, agent désactive tous les paramètres vocaux pour ces commandes, ainsi que les paramètres vocaux pour la [**légende**](caption-property.md) des objets [**Commands**](/windows/desktop/lwef/the-commands-collection-object) du client.</span><span class="sxs-lookup"><span data-stu-id="dc44c-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="dc44c-119">Cela vous permet de les éliminer de la grammaire active actuelle de votre client.</span><span class="sxs-lookup"><span data-stu-id="dc44c-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="dc44c-120">Toutefois, étant donné que cela bloque potentiellement l’accès vocal à d’autres clients, réinitialisez cette propriété sur **true** après avoir traité l’entrée vocale de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dc44c-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="dc44c-121">La désactivation de la propriété n’affecte pas le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="dc44c-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="dc44c-122">Les commandes globales ajoutées par le serveur s’affichent toujours.</span><span class="sxs-lookup"><span data-stu-id="dc44c-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="dc44c-123">Vous ne pouvez pas les supprimer du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="dc44c-123">You cannot remove them from the pop-up menu.</span></span>

 

