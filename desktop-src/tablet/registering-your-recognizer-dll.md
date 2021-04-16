---
description: Votre DLL de reconnaissance doit être inscrite pour que la plateforme Tablet PC l’utilise. Le module de reconnaissance doit apporter les modifications suivantes au registre lors de l’installation.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Inscription de votre DLL de module de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530274"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="056bf-104">Inscription de votre DLL de module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="056bf-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="056bf-105">Votre DLL de reconnaissance doit être inscrite pour que la plateforme Tablet PC l’utilise.</span><span class="sxs-lookup"><span data-stu-id="056bf-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="056bf-106">Le module de reconnaissance doit apporter les modifications suivantes au registre lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="056bf-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="056bf-107">Ajoutez une nouvelle clé pour chacun des CLSID de votre module de reconnaissance sous la clé de \_ Registre HKEY local \_ machine/Software/Microsoft/TPG/Recognizers/.</span><span class="sxs-lookup"><span data-stu-id="056bf-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="056bf-108">Ajoutez un CLSID par langue.</span><span class="sxs-lookup"><span data-stu-id="056bf-108">Add one CLSID per language.</span></span> <span data-ttu-id="056bf-109">Le tableau suivant décrit les valeurs qui doivent être ajoutées sous chacune des clés contenant vos CLSID.</span><span class="sxs-lookup"><span data-stu-id="056bf-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="056bf-110">Les noms de ces valeurs respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="056bf-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="056bf-111">Nom de la valeur</span><span class="sxs-lookup"><span data-stu-id="056bf-111">Value name</span></span>                             | <span data-ttu-id="056bf-112">Type de valeur</span><span class="sxs-lookup"><span data-stu-id="056bf-112">Value type</span></span>             | <span data-ttu-id="056bf-113">Description de la valeur</span><span class="sxs-lookup"><span data-stu-id="056bf-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056bf-114">Indicateurs de fonctionnalité de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="056bf-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="056bf-115">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="056bf-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="056bf-116">Valeur DWORD utilisée pour déterminer les fonctionnalités du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="056bf-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="056bf-117">DLL de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="056bf-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="056bf-118">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="056bf-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="056bf-119">Chemin d’accès complet à la DLL de reconnaissance installée.</span><span class="sxs-lookup"><span data-stu-id="056bf-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="056bf-120">Langues reconnues</span><span class="sxs-lookup"><span data-stu-id="056bf-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="056bf-121">\_fichier binaire reg</span><span class="sxs-lookup"><span data-stu-id="056bf-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="056bf-122">Tableau binaire décrivant le ou les langages avec lesquels un module de reconnaissance est conçu pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="056bf-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="056bf-123">Dans rectypes. h, la \_ définition Max languages définit spécifie le nombre maximal de langues prises en charge par un module de reconnaissance et chaque langue prend un mot à stocker dans l’élément « langues reconnues ».</span><span class="sxs-lookup"><span data-stu-id="056bf-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="056bf-124">La taille de l' \_ entrée de Registre reg Binary doit être Max \_ Language \* sizeof (Word).</span><span class="sxs-lookup"><span data-stu-id="056bf-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




