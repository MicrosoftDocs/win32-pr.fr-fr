---
description: Les fonctions suivantes sont utilisées avec l’échange de réseau.
ms.assetid: 5fd61759-1792-4db0-9ad4-adf112294b9c
title: Fonctions DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e5ae6a38ec6324cf33b4f9c4ffc1af44473699
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539342"
---
# <a name="network-dde-functions"></a><span data-ttu-id="de3f4-103">Fonctions DDE réseau</span><span class="sxs-lookup"><span data-stu-id="de3f4-103">Network DDE Functions</span></span>

<span data-ttu-id="de3f4-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="de3f4-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="de3f4-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="de3f4-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="de3f4-106">Les fonctions suivantes sont utilisées avec l’échange de réseau.</span><span class="sxs-lookup"><span data-stu-id="de3f4-106">The following functions are used with network DDE.</span></span>



| <span data-ttu-id="de3f4-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="de3f4-107">Function</span></span>                                                   | <span data-ttu-id="de3f4-108">Description</span><span class="sxs-lookup"><span data-stu-id="de3f4-108">Description</span></span>                                                                                                           |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de3f4-109">**NDdeGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="de3f4-109">**NDdeGetErrorString**</span></span>](nddegeterrorstring.md)           | <span data-ttu-id="de3f4-110">Convertit un code d’erreur retourné par une fonction DDE réseau en une chaîne d’erreur qui explique le code d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="de3f4-110">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span> |
| [<span data-ttu-id="de3f4-111">**NDdeGetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="de3f4-111">**NDdeGetShareSecurity**</span></span>](nddegetsharesecurity.md)       | <span data-ttu-id="de3f4-112">Récupère le descripteur de sécurité associé au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="de3f4-112">Retrieves the security descriptor associated with the DDE share.</span></span>                                                      |
| [<span data-ttu-id="de3f4-113">**NDdeGetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="de3f4-113">**NDdeGetTrustedShare**</span></span>](nddegettrustedshare.md)         | <span data-ttu-id="de3f4-114">Récupère les options associées à un partage DDE figurant dans la liste des partages approuvés de l’utilisateur du serveur.</span><span class="sxs-lookup"><span data-stu-id="de3f4-114">Retrieves the options associated with a DDE share that is in the server user's list of trusted shares.</span></span>                |
| [<span data-ttu-id="de3f4-115">**NDdeIsValidAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="de3f4-115">**NDdeIsValidAppTopicList**</span></span>](nddeisvalidapptopiclist.md) | <span data-ttu-id="de3f4-116">Détermine si une application et une chaîne de rubrique («*appname* \| *thème*») utilisent la syntaxe appropriée.</span><span class="sxs-lookup"><span data-stu-id="de3f4-116">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>                 |
| [<span data-ttu-id="de3f4-117">**NDdeIsValidShareName**</span><span class="sxs-lookup"><span data-stu-id="de3f4-117">**NDdeIsValidShareName**</span></span>](nddeisvalidsharename.md)       | <span data-ttu-id="de3f4-118">Détermine si un nom de partage utilise la syntaxe appropriée.</span><span class="sxs-lookup"><span data-stu-id="de3f4-118">Determines whether a share name uses the proper syntax.</span></span>                                                               |
| [<span data-ttu-id="de3f4-119">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="de3f4-119">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)       | <span data-ttu-id="de3f4-120">Définit le descripteur de sécurité associé au partage DDE.</span><span class="sxs-lookup"><span data-stu-id="de3f4-120">Sets the security descriptor associated with the DDE share.</span></span>                                                           |
| [<span data-ttu-id="de3f4-121">**NDdeSetTrustedShare**</span><span class="sxs-lookup"><span data-stu-id="de3f4-121">**NDdeSetTrustedShare**</span></span>](nddesettrustedshare.md)         | <span data-ttu-id="de3f4-122">Octroie l’état de confiance du partage DDE spécifié dans le contexte de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="de3f4-122">Grants the specified DDE share trusted status within the current user's context.</span></span>                                      |
| [<span data-ttu-id="de3f4-123">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="de3f4-123">**NDdeShareAdd**</span></span>](nddeshareadd.md)                       | <span data-ttu-id="de3f4-124">Crée et ajoute un nouveau partage DDE au gestionnaire de base de données du partage DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="de3f4-124">Creates and adds a new DDE share to the DDE share database manager (DSDM).</span></span>                                            |
| [<span data-ttu-id="de3f4-125">**NDdeShareDel**</span><span class="sxs-lookup"><span data-stu-id="de3f4-125">**NDdeShareDel**</span></span>](nddesharedel.md)                       | <span data-ttu-id="de3f4-126">Supprime un partage DDE du DSDM.</span><span class="sxs-lookup"><span data-stu-id="de3f4-126">Deletes a DDE share from the DSDM.</span></span>                                                                                    |
| [<span data-ttu-id="de3f4-127">**NDdeShareEnum**</span><span class="sxs-lookup"><span data-stu-id="de3f4-127">**NDdeShareEnum**</span></span>](nddeshareenum.md)                     | <span data-ttu-id="de3f4-128">Récupère la liste des partages DDE disponibles.</span><span class="sxs-lookup"><span data-stu-id="de3f4-128">Retrieves the list of available DDE shares.</span></span>                                                                           |
| [<span data-ttu-id="de3f4-129">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="de3f4-129">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)               | <span data-ttu-id="de3f4-130">Récupère les informations de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="de3f4-130">Retrieves DDE share information.</span></span>                                                                                      |
| [<span data-ttu-id="de3f4-131">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="de3f4-131">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)               | <span data-ttu-id="de3f4-132">Définit les informations de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="de3f4-132">Sets DDE share information.</span></span>                                                                                           |
| [<span data-ttu-id="de3f4-133">**NDdeTrustedShareEnum**</span><span class="sxs-lookup"><span data-stu-id="de3f4-133">**NDdeTrustedShareEnum**</span></span>](nddetrustedshareenum.md)       | <span data-ttu-id="de3f4-134">Récupère les noms de tous les partages DDE réseau approuvés dans le contexte du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="de3f4-134">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>                 |



 

 

 



