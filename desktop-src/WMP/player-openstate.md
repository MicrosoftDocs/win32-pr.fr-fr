---
title: Player. openState
description: La propriété openState récupère une valeur indiquant l’état de la source de contenu.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Lecteur Windows Media Player. openState
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532503"
---
# <a name="playeropenstate"></a><span data-ttu-id="8fbee-104">Player. openState</span><span class="sxs-lookup"><span data-stu-id="8fbee-104">Player.openState</span></span>

<span data-ttu-id="8fbee-105">La propriété **openState** récupère une valeur indiquant l’état de la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="8fbee-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fbee-106">Syntax</span></span>

<span data-ttu-id="8fbee-107">*lecteur* . **openState**</span><span class="sxs-lookup"><span data-stu-id="8fbee-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="8fbee-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8fbee-108">Possible Values</span></span>

<span data-ttu-id="8fbee-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="8fbee-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="8fbee-110">La constante d’énumération de style C peut être dérivée en préfixant la valeur d’État avec « wmpos ».</span><span class="sxs-lookup"><span data-stu-id="8fbee-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="8fbee-111">Par exemple, la constante de l’État PlaylistOpening est **wmposPlaylistOpening**.</span><span class="sxs-lookup"><span data-stu-id="8fbee-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="8fbee-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fbee-112">Value</span></span> | <span data-ttu-id="8fbee-113">State</span><span class="sxs-lookup"><span data-stu-id="8fbee-113">State</span></span>                   | <span data-ttu-id="8fbee-114">Description</span><span class="sxs-lookup"><span data-stu-id="8fbee-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbee-115">0</span><span class="sxs-lookup"><span data-stu-id="8fbee-115">0</span></span>     | <span data-ttu-id="8fbee-116">Indéfini</span><span class="sxs-lookup"><span data-stu-id="8fbee-116">Undefined</span></span>               | <span data-ttu-id="8fbee-117">Le lecteur Windows Media est dans un État non défini.</span><span class="sxs-lookup"><span data-stu-id="8fbee-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="8fbee-118">1</span><span class="sxs-lookup"><span data-stu-id="8fbee-118">1</span></span>     | <span data-ttu-id="8fbee-119">PlaylistChanging</span><span class="sxs-lookup"><span data-stu-id="8fbee-119">PlaylistChanging</span></span>        | <span data-ttu-id="8fbee-120">La nouvelle sélection va être chargée.</span><span class="sxs-lookup"><span data-stu-id="8fbee-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="8fbee-121">2</span><span class="sxs-lookup"><span data-stu-id="8fbee-121">2</span></span>     | <span data-ttu-id="8fbee-122">PlaylistLocating</span><span class="sxs-lookup"><span data-stu-id="8fbee-122">PlaylistLocating</span></span>        | <span data-ttu-id="8fbee-123">Le lecteur Windows Media tente de localiser la sélection.</span><span class="sxs-lookup"><span data-stu-id="8fbee-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="8fbee-124">La sélection peut être locale (bibliothèque ou métafichier avec une extension de nom de fichier. asx) ou distante.</span><span class="sxs-lookup"><span data-stu-id="8fbee-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="8fbee-125">3</span><span class="sxs-lookup"><span data-stu-id="8fbee-125">3</span></span>     | <span data-ttu-id="8fbee-126">PlaylistConnecting</span><span class="sxs-lookup"><span data-stu-id="8fbee-126">PlaylistConnecting</span></span>      | <span data-ttu-id="8fbee-127">Connexion à la sélection.</span><span class="sxs-lookup"><span data-stu-id="8fbee-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="8fbee-128">4</span><span class="sxs-lookup"><span data-stu-id="8fbee-128">4</span></span>     | <span data-ttu-id="8fbee-129">PlaylistLoading</span><span class="sxs-lookup"><span data-stu-id="8fbee-129">PlaylistLoading</span></span>         | <span data-ttu-id="8fbee-130">La sélection a été trouvée et est maintenant en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="8fbee-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="8fbee-131">5</span><span class="sxs-lookup"><span data-stu-id="8fbee-131">5</span></span>     | <span data-ttu-id="8fbee-132">PlaylistOpening</span><span class="sxs-lookup"><span data-stu-id="8fbee-132">PlaylistOpening</span></span>         | <span data-ttu-id="8fbee-133">La sélection a été récupérée et est maintenant en cours d’analyse et de chargement.</span><span class="sxs-lookup"><span data-stu-id="8fbee-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="8fbee-134">6</span><span class="sxs-lookup"><span data-stu-id="8fbee-134">6</span></span>     | <span data-ttu-id="8fbee-135">PlaylistOpenNoMedia</span><span class="sxs-lookup"><span data-stu-id="8fbee-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="8fbee-136">La sélection est ouverte.</span><span class="sxs-lookup"><span data-stu-id="8fbee-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="8fbee-137">7</span><span class="sxs-lookup"><span data-stu-id="8fbee-137">7</span></span>     | <span data-ttu-id="8fbee-138">PlaylistChanged</span><span class="sxs-lookup"><span data-stu-id="8fbee-138">PlaylistChanged</span></span>         | <span data-ttu-id="8fbee-139">Une nouvelle sélection a été affectée à **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="8fbee-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="8fbee-140">8</span><span class="sxs-lookup"><span data-stu-id="8fbee-140">8</span></span>     | <span data-ttu-id="8fbee-141">MediaChanging</span><span class="sxs-lookup"><span data-stu-id="8fbee-141">MediaChanging</span></span>           | <span data-ttu-id="8fbee-142">Un nouvel élément multimédia est sur le point d’être chargé.</span><span class="sxs-lookup"><span data-stu-id="8fbee-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="8fbee-143">9</span><span class="sxs-lookup"><span data-stu-id="8fbee-143">9</span></span>     | <span data-ttu-id="8fbee-144">MediaLocating</span><span class="sxs-lookup"><span data-stu-id="8fbee-144">MediaLocating</span></span>           | <span data-ttu-id="8fbee-145">Le lecteur Windows Media recherche l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8fbee-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="8fbee-146">Le fichier peut être local ou distant.</span><span class="sxs-lookup"><span data-stu-id="8fbee-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="8fbee-147">10</span><span class="sxs-lookup"><span data-stu-id="8fbee-147">10</span></span>    | <span data-ttu-id="8fbee-148">MediaConnecting</span><span class="sxs-lookup"><span data-stu-id="8fbee-148">MediaConnecting</span></span>         | <span data-ttu-id="8fbee-149">Connexion au serveur qui contient l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8fbee-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="8fbee-150">11</span><span class="sxs-lookup"><span data-stu-id="8fbee-150">11</span></span>    | <span data-ttu-id="8fbee-151">MediaLoading</span><span class="sxs-lookup"><span data-stu-id="8fbee-151">MediaLoading</span></span>            | <span data-ttu-id="8fbee-152">L’élément multimédia a été localisé et est maintenant en cours de récupération.</span><span class="sxs-lookup"><span data-stu-id="8fbee-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="8fbee-153">12</span><span class="sxs-lookup"><span data-stu-id="8fbee-153">12</span></span>    | <span data-ttu-id="8fbee-154">MediaOpening</span><span class="sxs-lookup"><span data-stu-id="8fbee-154">MediaOpening</span></span>            | <span data-ttu-id="8fbee-155">L’élément multimédia a été récupéré et est maintenant en cours d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="8fbee-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="8fbee-156">13</span><span class="sxs-lookup"><span data-stu-id="8fbee-156">13</span></span>    | <span data-ttu-id="8fbee-157">MediaOpen</span><span class="sxs-lookup"><span data-stu-id="8fbee-157">MediaOpen</span></span>               | <span data-ttu-id="8fbee-158">L’élément multimédia est maintenant ouvert.</span><span class="sxs-lookup"><span data-stu-id="8fbee-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="8fbee-159">14</span><span class="sxs-lookup"><span data-stu-id="8fbee-159">14</span></span>    | <span data-ttu-id="8fbee-160">BeginCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fbee-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="8fbee-161">Démarrage de l’acquisition du codec.</span><span class="sxs-lookup"><span data-stu-id="8fbee-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="8fbee-162">15</span><span class="sxs-lookup"><span data-stu-id="8fbee-162">15</span></span>    | <span data-ttu-id="8fbee-163">EndCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fbee-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="8fbee-164">L’acquisition du codec est terminée.</span><span class="sxs-lookup"><span data-stu-id="8fbee-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="8fbee-165">16</span><span class="sxs-lookup"><span data-stu-id="8fbee-165">16</span></span>    | <span data-ttu-id="8fbee-166">BeginLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fbee-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="8fbee-167">Acquisition d’une licence pour lire du contenu protégé par DRM.</span><span class="sxs-lookup"><span data-stu-id="8fbee-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="8fbee-168">17</span><span class="sxs-lookup"><span data-stu-id="8fbee-168">17</span></span>    | <span data-ttu-id="8fbee-169">EndLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fbee-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="8fbee-170">La licence de lecture de contenu DRM protégé a été acquise.</span><span class="sxs-lookup"><span data-stu-id="8fbee-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="8fbee-171">18</span><span class="sxs-lookup"><span data-stu-id="8fbee-171">18</span></span>    | <span data-ttu-id="8fbee-172">BeginIndividualization</span><span class="sxs-lookup"><span data-stu-id="8fbee-172">BeginIndividualization</span></span>  | <span data-ttu-id="8fbee-173">Commencez l’individualisation DRM.</span><span class="sxs-lookup"><span data-stu-id="8fbee-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="8fbee-174">19</span><span class="sxs-lookup"><span data-stu-id="8fbee-174">19</span></span>    | <span data-ttu-id="8fbee-175">EndIndividualization</span><span class="sxs-lookup"><span data-stu-id="8fbee-175">EndIndividualization</span></span>    | <span data-ttu-id="8fbee-176">L’individualisation DRM est terminée.</span><span class="sxs-lookup"><span data-stu-id="8fbee-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="8fbee-177">20</span><span class="sxs-lookup"><span data-stu-id="8fbee-177">20</span></span>    | <span data-ttu-id="8fbee-178">MediaWaiting</span><span class="sxs-lookup"><span data-stu-id="8fbee-178">MediaWaiting</span></span>            | <span data-ttu-id="8fbee-179">En attente d’un élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8fbee-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="8fbee-180">21</span><span class="sxs-lookup"><span data-stu-id="8fbee-180">21</span></span>    | <span data-ttu-id="8fbee-181">OpeningUnknownURL</span><span class="sxs-lookup"><span data-stu-id="8fbee-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="8fbee-182">Ouverture d’une URL avec un type inconnu.</span><span class="sxs-lookup"><span data-stu-id="8fbee-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8fbee-183">Notes</span><span class="sxs-lookup"><span data-stu-id="8fbee-183">Remarks</span></span>

<span data-ttu-id="8fbee-184">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="8fbee-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="8fbee-185">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="8fbee-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="8fbee-186">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="8fbee-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbee-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fbee-187">Requirements</span></span>



| <span data-ttu-id="8fbee-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fbee-188">Requirement</span></span> | <span data-ttu-id="8fbee-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fbee-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbee-190">Version</span><span class="sxs-lookup"><span data-stu-id="8fbee-190">Version</span></span><br/> | <span data-ttu-id="8fbee-191">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8fbee-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8fbee-192">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbee-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fbee-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbee-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbee-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fbee-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbee-195">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="8fbee-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="8fbee-196">**Événement Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="8fbee-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





