---
title: Propriété TTSModeID
description: Propriété TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197237"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="573ea-103">Propriété TTSModeID</span><span class="sxs-lookup"><span data-stu-id="573ea-103">TTSModeID Property</span></span>

<span data-ttu-id="573ea-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="573ea-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="573ea-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="573ea-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="573ea-106">Retourne ou définit le mode de moteur TTS utilisé pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="573ea-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="573ea-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="573ea-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="573ea-108">\*agent ***. Caractères («*** CharacterID \* \* * »). TTSModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="573ea-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="573ea-109">Partie</span><span class="sxs-lookup"><span data-stu-id="573ea-109">Part</span></span>     | <span data-ttu-id="573ea-110">Description</span><span class="sxs-lookup"><span data-stu-id="573ea-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="573ea-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="573ea-111">*ModeID*</span></span> | <span data-ttu-id="573ea-112">Expression de chaîne qui correspond à l’ID de mode d’un moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="573ea-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="573ea-113">Notes</span><span class="sxs-lookup"><span data-stu-id="573ea-113">Remarks</span></span>

<span data-ttu-id="573ea-114">Cette propriété détermine l’ID de mode de moteur TTS (conversion de texte par synthèse vocale) pour la sortie parlée d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="573ea-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="573ea-115">L’ID de mode pour un moteur TTS est une chaîne mise en forme définie par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur.</span><span class="sxs-lookup"><span data-stu-id="573ea-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="573ea-116">Pour plus d’informations, consultez [accès à un moteur de reconnaissance vocale dans votre code](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="573ea-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="573ea-117">La définition de cette propriété remplace la tentative du serveur de charger un moteur en fonction du paramètre TTS compilé du caractère et du paramètre [**LanguageID**](languageid-property.md) actuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="573ea-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="573ea-118">Toutefois, si vous spécifiez un ID de mode pour un moteur qui n’est pas installé ou si l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft (**AudioOutput. Enabled = False**), le serveur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="573ea-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="573ea-119">Si vous ne le faites pas (ou si vous n’avez pas réussi) à définir un ID de mode TTS pour le caractère, le serveur vérifie si le paramètre de mode TTS compilé du caractère correspond au paramètre [**LanguageID**](languageid-property.md) du caractère et que le moteur TTS associé est installé.</span><span class="sxs-lookup"><span data-stu-id="573ea-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="573ea-120">Si c’est le cas, le mode TTS utilisé par le caractère pour la sortie parlée et cette propriété retourne cet ID de mode.</span><span class="sxs-lookup"><span data-stu-id="573ea-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="573ea-121">Si ce n’est pas le cas, le serveur demande un moteur de reconnaissance vocale SAPI compatible qui correspond à l’ID de **langue** du caractère, ainsi que le sexe et l’âge définis pour l’ID du mode compilé du caractère.</span><span class="sxs-lookup"><span data-stu-id="573ea-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="573ea-122">Si vous n’avez pas défini l' **LanguageID** du caractère, son **LanguageID** correspond à la langue de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="573ea-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="573ea-123">Si aucun moteur correspondant n’est trouvé, l’interrogation de cette propriété retourne une chaîne vide pour l’ID de mode du moteur.</span><span class="sxs-lookup"><span data-stu-id="573ea-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="573ea-124">De même, si vous interrogez cette propriété lorsque l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft (**AudioOutput. Enabled = False**), la valeur sera une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="573ea-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="573ea-125">L’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé).</span><span class="sxs-lookup"><span data-stu-id="573ea-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="573ea-126">Toutefois, si le moteur spécifié dans le paramètre TTS compilé du caractère est installé et correspond au paramètre ID de langue du caractère, le moteur est chargé lorsque le caractère se charge.</span><span class="sxs-lookup"><span data-stu-id="573ea-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="573ea-127">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="573ea-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="573ea-128">La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech.</span><span class="sxs-lookup"><span data-stu-id="573ea-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="573ea-129">Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.</span><span class="sxs-lookup"><span data-stu-id="573ea-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="573ea-130">Cette propriété retourne également la chaîne vide si aucune prise en charge de son compatible n’est installée sur votre système.</span><span class="sxs-lookup"><span data-stu-id="573ea-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="573ea-131">La définition de **TTSModeID** peut échouer si Speech.dll n’est pas installé et que le moteur que vous spécifiez ne correspond pas au paramètre de mode TTS compilé du caractère.</span><span class="sxs-lookup"><span data-stu-id="573ea-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="573ea-132">L’interrogation de cette propriété ne retourne généralement pas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="573ea-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="573ea-133">Toutefois, si le temps de chargement du moteur de reconnaissance vocale est anormalement long, vous pouvez obtenir une erreur indiquant que la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="573ea-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="573ea-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="573ea-134">See Also</span></span>

[<span data-ttu-id="573ea-135">**LanguageID, propriété**</span><span class="sxs-lookup"><span data-stu-id="573ea-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




