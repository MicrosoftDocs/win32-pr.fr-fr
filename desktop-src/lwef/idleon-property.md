---
title: Propriété IdleOn
description: Propriété IdleOn
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309138"
---
# <a name="idleon-property"></a><span data-ttu-id="95fe6-103">Propriété IdleOn</span><span class="sxs-lookup"><span data-stu-id="95fe6-103">IdleOn Property</span></span>

<span data-ttu-id="95fe6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95fe6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="95fe6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="95fe6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="95fe6-106">Retourne ou définit une valeur booléenne qui détermine si le serveur gère les animations d’état **ralenti** du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="95fe6-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="95fe6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="95fe6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="95fe6-108">\*agent ***. Caractères («*** CharacterID \* \* * »). IdleOn* \*  \[  =  *booléen*\]</span><span class="sxs-lookup"><span data-stu-id="95fe6-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="95fe6-109">Partie</span><span class="sxs-lookup"><span data-stu-id="95fe6-109">Part</span></span>      | <span data-ttu-id="95fe6-110">Description</span><span class="sxs-lookup"><span data-stu-id="95fe6-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fe6-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="95fe6-111">*boolean*</span></span> | <span data-ttu-id="95fe6-112">Expression booléenne spécifiant si le serveur gère le mode inactif.</span><span class="sxs-lookup"><span data-stu-id="95fe6-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="95fe6-113">**True** (par défaut) la gestion du serveur de l’état inactif est activée.</span><span class="sxs-lookup"><span data-stu-id="95fe6-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="95fe6-114">**Valeur false** La gestion du serveur de l’état inactif est désactivée.</span><span class="sxs-lookup"><span data-stu-id="95fe6-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="95fe6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="95fe6-115">Remarks</span></span>

<span data-ttu-id="95fe6-116">Le serveur définit automatiquement un délai d’attente après la dernière animation lue pour un caractère.</span><span class="sxs-lookup"><span data-stu-id="95fe6-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="95fe6-117">Lorsque l’intervalle de ce minuteur est terminé, le serveur commence à l’état **ralenti** d’un caractère, en lisant ses animations de **ralenti** associées à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="95fe6-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="95fe6-118">Si vous souhaitez empêcher le serveur de lire automatiquement les animations d’état **ralenti** , affectez la valeur **false** à la propriété et lisez une animation ou appelez la méthode [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="95fe6-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="95fe6-119">La définition de cette valeur n’affecte pas l’état actuel de l’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="95fe6-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="95fe6-120">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="95fe6-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





