---
title: Gestion des erreurs avec les fonctions audio
description: Gestion des erreurs avec les fonctions audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimédia, erreurs audio de forme d’onde
- Erreurs audio, audio Wave
- audio multimédia, erreurs audio auxiliaires
- audio, erreurs audio auxiliaires
- sons Waveform, Erreurs
- audio auxiliaire, Erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314784"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="06b0f-109">Gestion des erreurs avec les fonctions audio</span><span class="sxs-lookup"><span data-stu-id="06b0f-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="06b0f-110">Les fonctions Wave-audio et auxiliaire-audio retournent une valeur différente de zéro lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="06b0f-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="06b0f-111">Windows fournit des fonctions qui convertissent ces valeurs d’erreur en descriptions textuelles des erreurs.</span><span class="sxs-lookup"><span data-stu-id="06b0f-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="06b0f-112">L’application doit toujours examiner les valeurs d’erreur pour déterminer comment procéder, mais les descriptions textuelles des erreurs peuvent être utilisées dans les boîtes de dialogue qui décrivent les erreurs aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="06b0f-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="06b0f-113">Vous pouvez utiliser les fonctions suivantes pour récupérer les descriptions textuelles des valeurs d’erreur audio :</span><span class="sxs-lookup"><span data-stu-id="06b0f-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="06b0f-114">Fonction</span><span class="sxs-lookup"><span data-stu-id="06b0f-114">Function</span></span>                                           | <span data-ttu-id="06b0f-115">Description</span><span class="sxs-lookup"><span data-stu-id="06b0f-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="06b0f-116">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="06b0f-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="06b0f-117">Récupère une description textuelle d’une erreur d’entrée audio Wave spécifiée.</span><span class="sxs-lookup"><span data-stu-id="06b0f-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="06b0f-118">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="06b0f-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="06b0f-119">Récupère une description textuelle d’une erreur de sortie Wave-Audio spécifiée.</span><span class="sxs-lookup"><span data-stu-id="06b0f-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="06b0f-120">Les seules fonctions audio qui ne retournent pas de valeurs d’erreur sont [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)et [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span><span class="sxs-lookup"><span data-stu-id="06b0f-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="06b0f-121">Ces fonctions retournent zéro si aucun appareil n’est présent dans un système ou si elles rencontrent des erreurs.</span><span class="sxs-lookup"><span data-stu-id="06b0f-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 