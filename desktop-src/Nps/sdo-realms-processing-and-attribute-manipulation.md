---
title: Traitement des domaines et manipulation des attributs
description: Le traitement des domaines, également appelé manipulation des attributs, fait référence à la transformation du nom de l’utilisateur qui demande l’accès.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd630fd683342c45ab35161bf2c740ac7e8a6fa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728565"
---
# <a name="realms-processing-and-attribute-manipulation"></a><span data-ttu-id="9f68b-103">Traitement des domaines et manipulation des attributs</span><span class="sxs-lookup"><span data-stu-id="9f68b-103">Realms Processing and Attribute Manipulation</span></span>

> [!Note]  
> <span data-ttu-id="9f68b-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9f68b-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="9f68b-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="9f68b-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="9f68b-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="9f68b-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="9f68b-107">Le traitement des domaines, également appelé manipulation des attributs, fait référence à la transformation du nom de l’utilisateur qui demande l’accès.</span><span class="sxs-lookup"><span data-stu-id="9f68b-107">Realms processing, which is also known as attribute manipulation, refers to transforming the name of the user requesting access.</span></span> <span data-ttu-id="9f68b-108">L’ID de station d’appel et l’ID de station appelée peuvent également être manipulés.</span><span class="sxs-lookup"><span data-stu-id="9f68b-108">The calling-station ID and called-station ID can also be manipulated.</span></span> <span data-ttu-id="9f68b-109">Les règles de traitement des domaines font partie de la collection d’attributs de profil proxy.</span><span class="sxs-lookup"><span data-stu-id="9f68b-109">The realms-processing rules are part of the Proxy profile attributes collection.</span></span>

<span data-ttu-id="9f68b-110">Pour chaque manipulation, vous devez créer deux attributs de [règle de manipulation](/windows/desktop/Nps/sdo-manipulation-rule) .</span><span class="sxs-lookup"><span data-stu-id="9f68b-110">For each manipulation, you need to create two [Manipulation-Rule](/windows/desktop/Nps/sdo-manipulation-rule) attributes.</span></span> <span data-ttu-id="9f68b-111">Chacun de ces attributs est une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9f68b-111">Each of these attributes is a string value.</span></span> <span data-ttu-id="9f68b-112">La première règle contient une expression régulière représentant le modèle à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="9f68b-112">The first rule contains a regular expression representing the pattern to match.</span></span> <span data-ttu-id="9f68b-113">La deuxième règle contient une expression régulière qui représente le texte de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9f68b-113">The second rule contains a regular expression representing the replacement text.</span></span> <span data-ttu-id="9f68b-114">Vous devez également créer un attribut [manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) .</span><span class="sxs-lookup"><span data-stu-id="9f68b-114">You must also create a [Manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) attribute.</span></span> <span data-ttu-id="9f68b-115">Cet attribut est une énumération qui spécifie quelle partie des informations de l’utilisateur doit être manipulée.</span><span class="sxs-lookup"><span data-stu-id="9f68b-115">This attribute is an enumeration that specifies which part of the user's information to manipulate.</span></span>

<span data-ttu-id="9f68b-116">L’ordre dans lequel les attributs sont créés est important.</span><span class="sxs-lookup"><span data-stu-id="9f68b-116">The order in which the attributes are created is important.</span></span> <span data-ttu-id="9f68b-117">NPS traite les attributs dans l’ordre dans lequel ils ont été créés.</span><span class="sxs-lookup"><span data-stu-id="9f68b-117">NPS processes the attributes in the order in which they were created.</span></span>

<span data-ttu-id="9f68b-118">Le tableau suivant montre un exemple d’un ensemble d’attributs de manipulation.</span><span class="sxs-lookup"><span data-stu-id="9f68b-118">The following table shows an example of a set of manipulation attributes.</span></span>



| <span data-ttu-id="9f68b-119">Nom</span><span class="sxs-lookup"><span data-stu-id="9f68b-119">Name</span></span>                 | <span data-ttu-id="9f68b-120">Type</span><span class="sxs-lookup"><span data-stu-id="9f68b-120">Type</span></span>         | <span data-ttu-id="9f68b-121">Valeur de chaîne</span><span class="sxs-lookup"><span data-stu-id="9f68b-121">String Value</span></span>     |
|----------------------|--------------|------------------|
| <span data-ttu-id="9f68b-122">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9f68b-122">msManipulationRule</span></span>   | <span data-ttu-id="9f68b-123">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="9f68b-123">**VT\_BSTR**</span></span> | <span data-ttu-id="9f68b-124">"@company.com"</span><span class="sxs-lookup"><span data-stu-id="9f68b-124">"@company.com"</span></span>   |
| <span data-ttu-id="9f68b-125">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9f68b-125">msManipulationRule</span></span>   | <span data-ttu-id="9f68b-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="9f68b-126">**VT\_BSTR**</span></span> | <span data-ttu-id="9f68b-127">"@microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="9f68b-127">"@microsoft.com"</span></span> |
| <span data-ttu-id="9f68b-128">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9f68b-128">msManipulationRule</span></span>   | <span data-ttu-id="9f68b-129">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="9f68b-129">**VT\_BSTR**</span></span> | <span data-ttu-id="9f68b-130">"^.+@"</span><span class="sxs-lookup"><span data-stu-id="9f68b-130">"^.+@"</span></span>           |
| <span data-ttu-id="9f68b-131">msManipulationRule</span><span class="sxs-lookup"><span data-stu-id="9f68b-131">msManipulationRule</span></span>   | <span data-ttu-id="9f68b-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="9f68b-132">**VT\_BSTR**</span></span> | <span data-ttu-id="9f68b-133">« guest@ »</span><span class="sxs-lookup"><span data-stu-id="9f68b-133">"guest@"</span></span>         |
| <span data-ttu-id="9f68b-134">msManipulationTarget</span><span class="sxs-lookup"><span data-stu-id="9f68b-134">msManipulationTarget</span></span> | <span data-ttu-id="9f68b-135">**VT \_**</span><span class="sxs-lookup"><span data-stu-id="9f68b-135">**VT\_I4**</span></span>   | <span data-ttu-id="9f68b-136">"1"</span><span class="sxs-lookup"><span data-stu-id="9f68b-136">"1"</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="9f68b-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9f68b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f68b-138">Hiérarchie du modèle objet</span><span class="sxs-lookup"><span data-stu-id="9f68b-138">Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="9f68b-139">Attributs pris en charge par SDO</span><span class="sxs-lookup"><span data-stu-id="9f68b-139">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[<span data-ttu-id="9f68b-140">Création d’une stratégie de demande de connexion</span><span class="sxs-lookup"><span data-stu-id="9f68b-140">Creating a Connection Request Policy</span></span>](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[<span data-ttu-id="9f68b-141">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="9f68b-141">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="9f68b-142">**ISdoDictionaryOld**</span><span class="sxs-lookup"><span data-stu-id="9f68b-142">**ISdoDictionaryOld**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[<span data-ttu-id="9f68b-143">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="9f68b-143">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 