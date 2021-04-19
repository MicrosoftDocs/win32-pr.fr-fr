---
title: Propriété SRModeID
description: Propriété SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511045"
---
# <a name="srmodeid-property"></a><span data-ttu-id="55abf-103">Propriété SRModeID</span><span class="sxs-lookup"><span data-stu-id="55abf-103">SRModeID Property</span></span>

<span data-ttu-id="55abf-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="55abf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="55abf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="55abf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="55abf-106">Retourne ou définit le moteur de reconnaissance vocale utilisé par le caractère.</span><span class="sxs-lookup"><span data-stu-id="55abf-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="55abf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="55abf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="55abf-108">\*agent ***. Caractères («*** CharacterID \* \* * »). SRModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="55abf-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="55abf-109">Partie</span><span class="sxs-lookup"><span data-stu-id="55abf-109">Part</span></span>     | <span data-ttu-id="55abf-110">Description</span><span class="sxs-lookup"><span data-stu-id="55abf-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="55abf-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="55abf-111">*ModeID*</span></span> | <span data-ttu-id="55abf-112">Expression de chaîne qui correspond à l’ID de mode d’un moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="55abf-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55abf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="55abf-113">Remarks</span></span>

<span data-ttu-id="55abf-114">La propriété détermine le moteur de reconnaissance vocale utilisé par le caractère pour l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="55abf-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="55abf-115">L’ID de mode d’un moteur de reconnaissance vocale est une chaîne mise en forme définie par le fournisseur de reconnaissance vocale qui identifie le moteur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="55abf-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="55abf-116">Pour plus d’informations, consultez [accès à un moteur de reconnaissance vocale dans votre code](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="55abf-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="55abf-117">Si vous spécifiez un ID de mode pour un moteur de reconnaissance vocale qui n’est pas installé, si l’utilisateur a désactivé la reconnaissance vocale (dans la feuille de propriétés de l’agent Microsoft), ou si la langue du moteur de reconnaissance vocale spécifié ne correspond pas au paramètre [**LanguageID**](languageid-property.md) du caractère, le serveur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="55abf-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="55abf-118">Si vous interrogez cette propriété et que vous n’avez pas encore défini le moteur de reconnaissance vocale, le serveur retourne l’ID de mode du moteur que SAPI retourne en fonction du paramètre [**LanguageID**](languageid-property.md) du caractère.</span><span class="sxs-lookup"><span data-stu-id="55abf-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="55abf-119">Si vous n’avez pas défini l’ID de **langue du caractère, agent** retourne l’ID de mode du moteur que SAPI retourne en fonction du paramètre d’ID de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55abf-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="55abf-120">S’il n’existe aucun moteur correspondant, le serveur retourne une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="55abf-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="55abf-121">L’interrogation de cette propriété ne requiert pas que [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) ait la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="55abf-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="55abf-122">Toutefois, si vous interrogez la propriété lorsque l’entrée vocale est désactivée, le serveur retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55abf-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="55abf-123">Lorsque l’entrée vocale est activée (dans la fenêtre Options de caractères avancés), l’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrera les services de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="55abf-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="55abf-124">Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable.</span><span class="sxs-lookup"><span data-stu-id="55abf-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="55abf-125">(La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.</span><span class="sxs-lookup"><span data-stu-id="55abf-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="55abf-126">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="55abf-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="55abf-127">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="55abf-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="55abf-128">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="55abf-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="55abf-129">Cette propriété retourne également la chaîne vide si aucune prise en charge de son compatible n’est installée sur votre système.</span><span class="sxs-lookup"><span data-stu-id="55abf-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="55abf-130">L’interrogation de cette propriété ne retourne généralement pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55abf-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="55abf-131">Toutefois, si le temps de chargement du moteur de reconnaissance vocale est anormalement long, vous pouvez obtenir une erreur indiquant que la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="55abf-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="55abf-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55abf-132">See Also</span></span>

[<span data-ttu-id="55abf-133">**LanguageID, propriété**</span><span class="sxs-lookup"><span data-stu-id="55abf-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




