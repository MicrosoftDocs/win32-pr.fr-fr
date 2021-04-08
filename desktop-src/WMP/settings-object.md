---
title: Settings (objet) (kit de développement logiciel Windows Media Player)
description: L’objet Settings permet de modifier différents paramètres du lecteur Windows Media à l’aide des propriétés et méthodes suivantes.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objet paramètres lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103841626"
---
# <a name="settings-object"></a><span data-ttu-id="233ea-104">Settings (objet)</span><span class="sxs-lookup"><span data-stu-id="233ea-104">Settings Object</span></span>

<span data-ttu-id="233ea-105">L’objet **Settings** permet de modifier différents paramètres du lecteur Windows Media à l’aide des propriétés et méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="233ea-105">The **Settings** object provides a way to modify various Windows Media Player settings by using the following properties and methods.</span></span>

<span data-ttu-id="233ea-106">L’objet **Settings** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="233ea-106">The **Settings** object supports the following properties.</span></span>



| <span data-ttu-id="233ea-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="233ea-107">Property</span></span>                                                  | <span data-ttu-id="233ea-108">Description</span><span class="sxs-lookup"><span data-stu-id="233ea-108">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="233ea-109">Démarrage automatique</span><span class="sxs-lookup"><span data-stu-id="233ea-109">autoStart</span></span>](settings-autostart.md)                       | <span data-ttu-id="233ea-110">Spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="233ea-110">Specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>                           |
| [<span data-ttu-id="233ea-111">équilibrée</span><span class="sxs-lookup"><span data-stu-id="233ea-111">balance</span></span>](settings-balance.md)                           | <span data-ttu-id="233ea-112">Spécifie ou récupère le solde stéréo actuel.</span><span class="sxs-lookup"><span data-stu-id="233ea-112">Specifies or retrieves the current stereo balance.</span></span>                                                                               |
| [<span data-ttu-id="233ea-113">baseURL</span><span class="sxs-lookup"><span data-stu-id="233ea-113">baseURL</span></span>](settings-baseurl.md)                           | <span data-ttu-id="233ea-114">Spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans des fichiers multimédias.</span><span class="sxs-lookup"><span data-stu-id="233ea-114">Specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media files.</span></span> |
| [<span data-ttu-id="233ea-115">defaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="233ea-115">defaultAudioLanguage</span></span>](settings-defaultaudiolanguage.md) | <span data-ttu-id="233ea-116">Récupère l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="233ea-116">Retrieves the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>                          |
| [<span data-ttu-id="233ea-117">defaultFrame</span><span class="sxs-lookup"><span data-stu-id="233ea-117">defaultFrame</span></span>](settings-defaultframe.md)                 | <span data-ttu-id="233ea-118">Spécifie ou récupère le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="233ea-118">Specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>                |
| [<span data-ttu-id="233ea-119">enableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="233ea-119">enableErrorDialogs</span></span>](settings-enableerrordialogs.md)     | <span data-ttu-id="233ea-120">Spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.</span><span class="sxs-lookup"><span data-stu-id="233ea-120">Specifies or retrieves a value indicating whether error dialog boxes are shown automatically.</span></span>                                    |
| [<span data-ttu-id="233ea-121">invokeURLs</span><span class="sxs-lookup"><span data-stu-id="233ea-121">invokeURLs</span></span>](settings-invokeurls.md)                     | <span data-ttu-id="233ea-122">Spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="233ea-122">Specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>                                        |
| [<span data-ttu-id="233ea-123">isAvailable</span><span class="sxs-lookup"><span data-stu-id="233ea-123">isAvailable</span></span>](settings-isavailable.md)                   | <span data-ttu-id="233ea-124">Récupère une valeur indiquant si un type d’informations spécifié est disponible ou si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="233ea-124">Retrieves whether a specified type of information is available or a specified action can be performed.</span></span>                           |
| [<span data-ttu-id="233ea-125">mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="233ea-125">mediaAccessRights</span></span>](settings-mediaaccessrights.md)       | <span data-ttu-id="233ea-126">Récupère une valeur indiquant les droits actuellement accordés pour l’accès à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="233ea-126">Retrieves a value indicating the rights currently granted for library access.</span></span>                                                    |
| [<span data-ttu-id="233ea-127">muette</span><span class="sxs-lookup"><span data-stu-id="233ea-127">mute</span></span>](settings-mute.md)                                 | <span data-ttu-id="233ea-128">Spécifie ou récupère une valeur indiquant si l’audio est muet.</span><span class="sxs-lookup"><span data-stu-id="233ea-128">Specifies or retrieves a value indicating whether audio is muted.</span></span>                                                                |
| [<span data-ttu-id="233ea-129">playCount</span><span class="sxs-lookup"><span data-stu-id="233ea-129">playCount</span></span>](settings-playcount.md)                       | <span data-ttu-id="233ea-130">Spécifie ou récupère le nombre de fois qu’un élément multimédia doit être lu.</span><span class="sxs-lookup"><span data-stu-id="233ea-130">Specifies or retrieves the number of times a media item will play.</span></span>                                                               |
| [<span data-ttu-id="233ea-131">évaluation</span><span class="sxs-lookup"><span data-stu-id="233ea-131">rate</span></span>](settings-rate.md)                                 | <span data-ttu-id="233ea-132">Spécifie ou récupère la vitesse de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="233ea-132">Specifies or retrieves the current playback rate.</span></span>                                                                                |
| [<span data-ttu-id="233ea-133">volume</span><span class="sxs-lookup"><span data-stu-id="233ea-133">volume</span></span>](settings-volume.md)                             | <span data-ttu-id="233ea-134">Spécifie ou récupère le volume actuel.</span><span class="sxs-lookup"><span data-stu-id="233ea-134">Specifies or retrieves the current volume.</span></span>                                                                                       |



 

<span data-ttu-id="233ea-135">L’objet **Settings** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="233ea-135">The **Settings** object supports the following methods.</span></span>



| <span data-ttu-id="233ea-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="233ea-136">Method</span></span>                                                            | <span data-ttu-id="233ea-137">Description</span><span class="sxs-lookup"><span data-stu-id="233ea-137">Description</span></span>                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="233ea-138">getMode</span><span class="sxs-lookup"><span data-stu-id="233ea-138">getMode</span></span>](settings-getmode.md)                                   | <span data-ttu-id="233ea-139">Détermine si le mode de boucle ou le mode de lecture aléatoire est actif.</span><span class="sxs-lookup"><span data-stu-id="233ea-139">Determines whether the loop mode or shuffle mode is active.</span></span> |
| [<span data-ttu-id="233ea-140">requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="233ea-140">requestMediaAccessRights</span></span>](settings-requestmediaaccessrights.md) | <span data-ttu-id="233ea-141">Demande un niveau d’accès spécifié à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="233ea-141">Requests a specified level of access to the library.</span></span>        |
| [<span data-ttu-id="233ea-142">setMode</span><span class="sxs-lookup"><span data-stu-id="233ea-142">setMode</span></span>](settings-setmode.md)                                   | <span data-ttu-id="233ea-143">Définit le mode de boucle ou le mode de lecture aléatoire (actif ou inactif).</span><span class="sxs-lookup"><span data-stu-id="233ea-143">Sets the loop mode or shuffle mode to active or inactive.</span></span>   |



 

<span data-ttu-id="233ea-144">L’objet **Settings** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="233ea-144">The **Settings** object is accessed through the following property.</span></span>



| <span data-ttu-id="233ea-145">Object</span><span class="sxs-lookup"><span data-stu-id="233ea-145">Object</span></span>                      | <span data-ttu-id="233ea-146">Propriété</span><span class="sxs-lookup"><span data-stu-id="233ea-146">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="233ea-147">Lecteur</span><span class="sxs-lookup"><span data-stu-id="233ea-147">Player</span></span>](player-object.md) | [<span data-ttu-id="233ea-148">settings</span><span class="sxs-lookup"><span data-stu-id="233ea-148">settings</span></span>](player-settings.md) |



 

## <a name="see-also"></a><span data-ttu-id="233ea-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="233ea-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233ea-150">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="233ea-150">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




