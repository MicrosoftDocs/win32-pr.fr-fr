---
title: Types d’utilisateurs inconnus
description: Types d’utilisateurs inconnus
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316577"
---
# <a name="unknown-user-types"></a><span data-ttu-id="d5640-103">Types d’utilisateurs inconnus</span><span class="sxs-lookup"><span data-stu-id="d5640-103">Unknown User Types</span></span>

<span data-ttu-id="d5640-104">Vous pouvez faciliter la localisation du produit en ajoutant la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="d5640-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="d5640-105">**HKEY \_ \_Ordinateurs locaux \\ logiciel \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*</span><span class="sxs-lookup"><span data-stu-id="d5640-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="d5640-106">Cette clé permet aux fonctions de retourner une chaîne spécifiée plutôt qu’une valeur par défaut « Unknown », ce qui permet aux localisateurs de spécifier un type d’utilisateur d’une langue différente.</span><span class="sxs-lookup"><span data-stu-id="d5640-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="d5640-107">L’implémentation du gestionnaire par défaut COM de [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examine le registre en appelant [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="d5640-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="d5640-108">Si la classe de l’objet est introuvable dans le registre, le type d’utilisateur de l’instance [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) de l’objet est retourné.</span><span class="sxs-lookup"><span data-stu-id="d5640-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="d5640-109">Si la classe est introuvable dans l’instance **IStorage** de l’objet, la chaîne « Unknown » est retournée.</span><span class="sxs-lookup"><span data-stu-id="d5640-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5640-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5640-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5640-111">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="d5640-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 