---
description: Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objet WebWizardHost (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951926"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="2335b-103">Objet WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="2335b-103">WebWizardHost object</span></span>

<span data-ttu-id="2335b-104">Expose des méthodes qui activent des pages HTML hébergées dans une extension d’Assistant pour communiquer avec l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="2335b-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="2335b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2335b-105">Members</span></span>

<span data-ttu-id="2335b-106">L’objet **WebWizardHost** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2335b-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="2335b-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2335b-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="2335b-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2335b-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2335b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2335b-109">Methods</span></span>

<span data-ttu-id="2335b-110">L’objet **WebWizardHost** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2335b-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="2335b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="2335b-111">Method</span></span>                                                      | <span data-ttu-id="2335b-112">Description</span><span class="sxs-lookup"><span data-stu-id="2335b-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2335b-113">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="2335b-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="2335b-114">Simule un clic sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="2335b-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="2335b-115">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="2335b-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="2335b-116">Accède à la page côté client qui précède immédiatement la page hébergeant les pages HTML côté serveur.</span><span class="sxs-lookup"><span data-stu-id="2335b-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="2335b-117">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="2335b-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="2335b-118">Accède à la page de l’Assistant côté client qui suit la page qui héberge les pages HTML côté serveur, ou termine l’Assistant s’il n’y a pas d’autres pages côté client.</span><span class="sxs-lookup"><span data-stu-id="2335b-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="2335b-119">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="2335b-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="2335b-120">Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="2335b-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="2335b-121">En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="2335b-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="2335b-122">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="2335b-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="2335b-123">Met à jour les boutons **précédent**, **suivant** et **Terminer** dans le frame de l’Assistant du client.</span><span class="sxs-lookup"><span data-stu-id="2335b-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="2335b-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2335b-124">Properties</span></span>

<span data-ttu-id="2335b-125">L’objet **WebWizardHost** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2335b-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="2335b-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="2335b-126">Property</span></span>                                               | <span data-ttu-id="2335b-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2335b-127">Access type</span></span>           | <span data-ttu-id="2335b-128">Description</span><span class="sxs-lookup"><span data-stu-id="2335b-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="2335b-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2335b-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="2335b-130">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2335b-130">Read/write</span></span><br/> | <span data-ttu-id="2335b-131">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="2335b-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="2335b-132">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="2335b-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="2335b-133">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2335b-133">Read/write</span></span><br/> | <span data-ttu-id="2335b-134">Définit ou récupère la valeur actuelle d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="2335b-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2335b-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2335b-135">Requirements</span></span>



| <span data-ttu-id="2335b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2335b-136">Requirement</span></span> | <span data-ttu-id="2335b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2335b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2335b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2335b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2335b-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2335b-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2335b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2335b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2335b-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2335b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2335b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="2335b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2335b-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2335b-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2335b-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="2335b-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2335b-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2335b-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2335b-146">IID</span><span class="sxs-lookup"><span data-stu-id="2335b-146">IID</span></span><br/>                      | <span data-ttu-id="2335b-147">CLSID \_ WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="2335b-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




