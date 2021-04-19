---
title: Méthode Play (fonctionnalités héritées de l’environnement Windows)
description: Méthode Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511529"
---
# <a name="play-method-legacy-windows-environment-features"></a><span data-ttu-id="05152-103">Méthode Play (fonctionnalités héritées de l’environnement Windows)</span><span class="sxs-lookup"><span data-stu-id="05152-103">Play Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="05152-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05152-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="05152-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="05152-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="05152-106">Lit l’animation spécifiée pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="05152-106">Plays the specified animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="05152-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="05152-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="05152-108">\*agent \***. Caractères («**_CharacterID_*_»). Play_* «*AnimationName*»</span><span class="sxs-lookup"><span data-stu-id="05152-108">*agent\***.Characters ("**_CharacterID_*_").Play_\* "*AnimationName*"</span></span>

</dd> </dl> 

| <span data-ttu-id="05152-109">Partie</span><span class="sxs-lookup"><span data-stu-id="05152-109">Part</span></span>            | <span data-ttu-id="05152-110">Description</span><span class="sxs-lookup"><span data-stu-id="05152-110">Description</span></span>                                                          |
|-----------------|----------------------------------------------------------------------|
| <span data-ttu-id="05152-111">*AnimationName*</span><span class="sxs-lookup"><span data-stu-id="05152-111">*AnimationName*</span></span> | <span data-ttu-id="05152-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="05152-112">Required.</span></span> <span data-ttu-id="05152-113">Chaîne qui spécifie le nom d’une séquence d’animation.</span><span class="sxs-lookup"><span data-stu-id="05152-113">A string that specifies the name of an animation sequence.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="05152-114">Notes</span><span class="sxs-lookup"><span data-stu-id="05152-114">Remarks</span></span>

<span data-ttu-id="05152-115">Le nom d’une animation est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="05152-115">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="05152-116">Avant de lire l’animation spécifiée, le serveur tente de lire l’animation de **retour** pour l’animation précédente, si celle-ci a été assignée.</span><span class="sxs-lookup"><span data-stu-id="05152-116">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation, if one has been assigned.</span></span>

<span data-ttu-id="05152-117">Lors de l’accès aux animations d’un caractère à l’aide d’un protocole de fichier conventionnel, vous pouvez simplement utiliser la méthode **Play** en spécifiant le nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="05152-117">When accessing a character's animations using a conventional file protocol, you can simply use the **Play** method specifying the name of the animation.</span></span> <span data-ttu-id="05152-118">Toutefois, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' **extraction** pour charger l’animation avant d’appeler la méthode **Play** .</span><span class="sxs-lookup"><span data-stu-id="05152-118">However, if you are using the HTTP protocol to access character animation data, use the **Get** method to load the animation before calling the **Play** method.</span></span>

<span data-ttu-id="05152-119">Pour plus d’informations, consultez la méthode **obtenir** .</span><span class="sxs-lookup"><span data-stu-id="05152-119">For more information, see the **Get** method.</span></span>

<span data-ttu-id="05152-120">Pour simplifier votre syntaxe, vous pouvez déclarer une référence d’objet et la définir pour faire référence à l’objet de [**caractère**](/windows/desktop/lwef/the-characters-object) dans la collection de [**caractères**](/windows/desktop/lwef/the-characters-object) et utiliser la référence dans le cadre de vos instructions de **lecture** :</span><span class="sxs-lookup"><span data-stu-id="05152-120">To simplify your syntax, you can declare an object reference and set it to reference the [**Character**](/windows/desktop/lwef/the-characters-object) object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection and use the reference as part of your **Play** statements:</span></span>


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



<span data-ttu-id="05152-121">Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="05152-121">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="05152-122">En outre, si vous spécifiez une animation qui n’est pas chargée ou si le caractère n’a pas été chargé avec succès, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » avec un numéro d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="05152-122">In addition, if you specify an animation that is not loaded or if the character has not been successfully loaded, the server sets the [**Status**](status-property.md) property of **Request** object to "failed" with an appropriate error number.</span></span> <span data-ttu-id="05152-123">Toutefois, si l’animation n’existe pas et que les données du caractère ont déjà été chargées avec succès, le serveur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="05152-123">However, if the animation does not exist and the character's data has already been successfully loaded, the server raises an error.</span></span>

<span data-ttu-id="05152-124">La méthode **Play** ne rend pas visible le caractère.</span><span class="sxs-lookup"><span data-stu-id="05152-124">The **Play** method does not make the character visible.</span></span> <span data-ttu-id="05152-125">Si le caractère n’est pas visible, le serveur lit l’animation de manière invisible et définit la propriété [**Status**](status-property.md) de l’objet de [**requête**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="05152-125">If the character is not visible, the server plays the animation invisibly, and sets the [**Status**](status-property.md) property of the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 
