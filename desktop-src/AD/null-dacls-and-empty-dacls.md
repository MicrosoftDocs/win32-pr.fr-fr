---
title: DACL null et DACL vides (AD DS)
description: La présence d’une liste de contrôle d’accès discrétionnaire null dans l’attribut nTSecurityDescriptor d’un objet peut créer un risque de sécurité grave.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL null et listes DACL vides
- DACL AD, NULL et Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940804"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a><span data-ttu-id="3f1ee-105">DACL null et DACL vides (AD DS)</span><span class="sxs-lookup"><span data-stu-id="3f1ee-105">Null DACLs and Empty DACLs (AD DS)</span></span>

<span data-ttu-id="3f1ee-106">La présence d’une liste de contrôle d’accès discrétionnaire null dans l’attribut [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) d’un objet peut créer un risque de sécurité grave.</span><span class="sxs-lookup"><span data-stu-id="3f1ee-106">The presence of a null discretionary access-control list (DACL) in the [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) attribute of any object can create a serious security risk.</span></span> <span data-ttu-id="3f1ee-107">Une liste DACL null accorde un accès complet à tout utilisateur qui la demande ; la vérification de sécurité normale n’est pas effectuée par rapport à l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f1ee-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="3f1ee-108">Une DACL NULL ne doit pas être confondue avec une liste DACL vide.</span><span class="sxs-lookup"><span data-stu-id="3f1ee-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="3f1ee-109">Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune entrée de contrôle d’accès (ACE).</span><span class="sxs-lookup"><span data-stu-id="3f1ee-109">An empty DACL is a properly allocated and initialized DACL containing no access-control entries (ACEs).</span></span> <span data-ttu-id="3f1ee-110">Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.</span><span class="sxs-lookup"><span data-stu-id="3f1ee-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="3f1ee-111">Pour plus d’informations, consultez [DACL null et DACL vides](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="3f1ee-111">For more information, see [Null DACLs and Empty DACLs](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).</span></span>

 

 