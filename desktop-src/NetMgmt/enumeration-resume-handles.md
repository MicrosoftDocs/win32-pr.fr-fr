---
title: Handles de reprise d’énumération
description: Les handles de reprise d’énumération sont des identificateurs pour la clé de reprise réelle contenue dans les données d’instance de la fonction. Cela est nécessaire pour la sécurité, l’interopérabilité et pour simplifier le code de l’appelant pour la fonction.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939993"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="32c3f-104">Handles de reprise d’énumération</span><span class="sxs-lookup"><span data-stu-id="32c3f-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="32c3f-105">Les handles de reprise d’énumération sont des identificateurs pour la clé de reprise réelle contenue dans les données d’instance de la fonction.</span><span class="sxs-lookup"><span data-stu-id="32c3f-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="32c3f-106">Cela est nécessaire pour la sécurité, l’interopérabilité et pour simplifier le code de l’appelant pour la fonction.</span><span class="sxs-lookup"><span data-stu-id="32c3f-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="32c3f-107">Si une **valeur null** est transmise pour le pointeur vers le handle de reprise, aucun handle n’est stocké et la recherche d’énumération ne peut pas être poursuivie.</span><span class="sxs-lookup"><span data-stu-id="32c3f-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="32c3f-108">Cela est utile dans les cas où l’application ne souhaite pas énumérer tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="32c3f-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="32c3f-109">Si une erreur est retournée à partir d’un appel d’énumération, le handle de reprise doit être traité comme non valide et n’est pas utilisé pour les appels d’énumération suivants.</span><span class="sxs-lookup"><span data-stu-id="32c3f-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="32c3f-110">Lorsque cela se produit, vous devez redémarrer l’énumération depuis le début.</span><span class="sxs-lookup"><span data-stu-id="32c3f-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




