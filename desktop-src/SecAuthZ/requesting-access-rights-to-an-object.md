---
description: Lorsque vous ouvrez un handle vers un objet, le handle retourné a une combinaison de droits d’accès à l’objet.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Demande de droits d’accès à un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515068"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="dd879-103">Demande de droits d’accès à un objet</span><span class="sxs-lookup"><span data-stu-id="dd879-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="dd879-104">Lorsque vous ouvrez un handle vers un objet, le handle retourné a une combinaison de droits d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dd879-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="dd879-105">Certaines fonctions, telles que [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), ne nécessitent pas un ensemble spécifique de droits d’accès demandés.</span><span class="sxs-lookup"><span data-stu-id="dd879-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="dd879-106">Ces fonctions essaient toujours d’ouvrir le descripteur pour un accès complet.</span><span class="sxs-lookup"><span data-stu-id="dd879-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="dd879-107">D’autres fonctions, telles que [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) et [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), vous permettent de spécifier le jeu de droits d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="dd879-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="dd879-108">Vous devez demander uniquement les droits d’accès dont vous avez besoin, plutôt que d’ouvrir un handle pour un accès complet.</span><span class="sxs-lookup"><span data-stu-id="dd879-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="dd879-109">Cela empêche l’utilisation du descripteur de façon inattendue et augmente les chances que la demande d’accès aboutisse si le DACL de l’objet n’autorise que l’accès limité.</span><span class="sxs-lookup"><span data-stu-id="dd879-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="dd879-110">Utilisez les [droits d’accès génériques](generic-access-rights.md) pour spécifier le type d’accès nécessaire lors de l’ouverture d’un handle vers un objet.</span><span class="sxs-lookup"><span data-stu-id="dd879-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="dd879-111">C’est généralement plus simple que de spécifier tous les droits standard et spécifiques correspondants.</span><span class="sxs-lookup"><span data-stu-id="dd879-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="dd879-112">Vous pouvez également utiliser la \_ constante maximale autorisée pour demander à ce que l’objet soit ouvert avec tous les droits d’accès valides pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dd879-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="dd879-113">La \_ constante maximale autorisée ne peut pas être utilisée dans une entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="dd879-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="dd879-114">Pour obtenir ou définir la liste SACL dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet, demandez le droit accès à la [ \_ \_ sécurité du système Access](sacl-access-right.md) lors de l’ouverture d’un handle vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="dd879-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
