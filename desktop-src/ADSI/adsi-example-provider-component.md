---
title: Composant fournisseur d’exemples ADSI
description: Les rédacteurs du fournisseur d’interfaces de service Active Directory trouveront cette section particulièrement intéressante, car il décrit en détail le composant fournisseur d’exemples ADSI.
ms.assetid: 1ca73817-7a21-4a39-b496-fc82db26ea4e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7bf960021df9a3b26f252584cad2ff3374254a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309266"
---
# <a name="adsi-example-provider-component"></a><span data-ttu-id="d4efc-103">Composant fournisseur d’exemples ADSI</span><span class="sxs-lookup"><span data-stu-id="d4efc-103">ADSI Example Provider Component</span></span>

<span data-ttu-id="d4efc-104">Les rédacteurs du fournisseur d’interfaces de service Active Directory trouveront cette section particulièrement intéressante, car il décrit en détail le composant fournisseur d’exemples ADSI.</span><span class="sxs-lookup"><span data-stu-id="d4efc-104">Active Directory Service Interfaces provider writers will find this section of particular interest, because it describes the ADSI example provider component in depth.</span></span> <span data-ttu-id="d4efc-105">Les rédacteurs de fournisseur ADSI peuvent installer l’exemple de fournisseur et utiliser l’infrastructure de code comme base pour créer leur propre implémentation.</span><span class="sxs-lookup"><span data-stu-id="d4efc-105">ADSI provider writers can install the example provider and use the code framework as a basis to create their own implementation.</span></span> <span data-ttu-id="d4efc-106">Les rubriques suivantes sont présentées :</span><span class="sxs-lookup"><span data-stu-id="d4efc-106">The following topics are discussed:</span></span>

<span data-ttu-id="d4efc-107">[Installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md) décrit comment installer l’exemple de fournisseur ADSI et son répertoire factice.</span><span class="sxs-lookup"><span data-stu-id="d4efc-107">[Installing the Example Provider Component](installing-the-example-provider-component.md) describes how to install the ADSI sample provider and its mock directory.</span></span> <span data-ttu-id="d4efc-108">Cette section comprend une liste des paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="d4efc-108">This section includes a list of the registry settings.</span></span>

<span data-ttu-id="d4efc-109">[Définition de répertoire](directory-definition.md) décrit les entrées de répertoire définies par l’exemple de composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d4efc-109">[Directory Definition](directory-definition.md) describes the directory entries defined by the example provider component.</span></span>

<span data-ttu-id="d4efc-110">La [gestion de schéma](schema-management.md) décrit la façon dont chaque élément de l’exemple de service d’annuaire de composant fournisseur peut être représenté par un type spécifique d’Active Directory objet.</span><span class="sxs-lookup"><span data-stu-id="d4efc-110">[Schema Management](schema-management.md) describes how each element in the example provider component directory service can be represented by a specific type of Active Directory object.</span></span>

<span data-ttu-id="d4efc-111">La [liaison à un objet Active Directory](binding-to-an-active-directory-object.md) décrit comment, étant donné une chaîne ADsPath, l’exemple de composant fournisseur identifie cet élément, crée le type approprié d’Active Directory objet pour celui-ci et récupère le type demandé de pointeur d’interface sur cet objet à retourner au logiciel client ads.</span><span class="sxs-lookup"><span data-stu-id="d4efc-111">[Binding to an Active Directory Object](binding-to-an-active-directory-object.md) describes how, given an ADsPath string, the example provider component identifies that element, creates the appropriate type of Active Directory object for it, and retrieves the requested type of interface pointer on that object to pass back to the ADs client software.</span></span>

<span data-ttu-id="d4efc-112">[Objets Enumerator](enumerator-objects.md) répertorie les types spécifiques d’énumérations fournis par le composant de fournisseur d’exemple et le code source dans lequel les implémentations peuvent être trouvées.</span><span class="sxs-lookup"><span data-stu-id="d4efc-112">[Enumerator Objects](enumerator-objects.md) lists the specific types of enumerations supplied by the example provider component and in which source code the implementations can be found.</span></span>

<span data-ttu-id="d4efc-113">La [vue d’ensemble du code](code-overview.md) fournit une description au niveau des tâches de chaque partie de l’exemple de composant fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d4efc-113">[Code Overview](code-overview.md) provides a task-level description of each part of the example provider component.</span></span>

<span data-ttu-id="d4efc-114">[Détails du code](code-details.md) répertorie les modules logiciels et leur contenu.</span><span class="sxs-lookup"><span data-stu-id="d4efc-114">[Code Details](code-details.md) lists the software modules and their contents.</span></span>

 

 




