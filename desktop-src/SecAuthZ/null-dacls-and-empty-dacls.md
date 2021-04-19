---
description: Une liste DACL null accorde un accès complet à tous les utilisateurs qui le demandent. Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune entrée de contrôle d’accès. Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL null et DACL vides (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536830"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="65ba8-105">DACL null et DACL vides (autorisation)</span><span class="sxs-lookup"><span data-stu-id="65ba8-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="65ba8-106">Si la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) qui appartient au [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) d’un objet a la valeur **null**, une DACL null est créée.</span><span class="sxs-lookup"><span data-stu-id="65ba8-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="65ba8-107">Une liste DACL null accorde un accès complet à tout utilisateur qui la demande ; la vérification de sécurité normale n’est pas effectuée par rapport à l’objet.</span><span class="sxs-lookup"><span data-stu-id="65ba8-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="65ba8-108">Une DACL NULL ne doit pas être confondue avec une liste DACL vide.</span><span class="sxs-lookup"><span data-stu-id="65ba8-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="65ba8-109">Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE).</span><span class="sxs-lookup"><span data-stu-id="65ba8-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="65ba8-110">Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.</span><span class="sxs-lookup"><span data-stu-id="65ba8-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="65ba8-111">Pour obtenir un exemple de création d’une liste DACL, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="65ba8-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 
