---
title: Méthode Stop (fonctionnalités héritées de l’environnement Windows)
description: Stop, méthode
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106527563"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="b2a2a-103">Méthode Stop (fonctionnalités héritées de l’environnement Windows)</span><span class="sxs-lookup"><span data-stu-id="b2a2a-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="b2a2a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2a2a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b2a2a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="b2a2a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b2a2a-106">Arrête l’animation pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="b2a2a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="b2a2a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b2a2a-108">\*agent \***. Caractères («**_CharacterID_\*_»). Arrêter_ la \*  \[ *requête*\]</span><span class="sxs-lookup"><span data-stu-id="b2a2a-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="b2a2a-109">Partie</span><span class="sxs-lookup"><span data-stu-id="b2a2a-109">Part</span></span>      | <span data-ttu-id="b2a2a-110">Description</span><span class="sxs-lookup"><span data-stu-id="b2a2a-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a2a-111">*Requête*</span><span class="sxs-lookup"><span data-stu-id="b2a2a-111">*Request*</span></span> | <span data-ttu-id="b2a2a-112">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-112">Optional.</span></span> <span data-ttu-id="b2a2a-113">Objet de [**requête**](/windows/desktop/lwef/the-request-object) spécifiant un appel d’animation particulier.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2a2a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b2a2a-114">Remarks</span></span>

<span data-ttu-id="b2a2a-115">Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez arrêter.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="b2a2a-116">Si vous ne définissez pas le paramètre de **requête** , le serveur arrête toutes les animations pour le caractère, y compris [**les appels de**](get-method.md) mise en file d’attente, et efface sa file d’attente d’animation, sauf si le caractère est en train de lire son **masquage** ou d' **Afficher** l’animation.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="b2a2a-117">Cette méthode n’arrête pas les appels d' **extraction** non mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="b2a2a-118">Pour arrêter une animation ou [**obtenir**](get-method.md) un appel spécifique, déclarez une variable objet et affectez votre demande d’animation à cette variable :</span><span class="sxs-lookup"><span data-stu-id="b2a2a-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="b2a2a-119">Cette méthode ne génère pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b2a2a-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2a2a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2a2a-120">See Also</span></span>

[<span data-ttu-id="b2a2a-121">**StopAll, méthode**</span><span class="sxs-lookup"><span data-stu-id="b2a2a-121">**StopAll method**</span></span>](stopall-method.md)


 

 
