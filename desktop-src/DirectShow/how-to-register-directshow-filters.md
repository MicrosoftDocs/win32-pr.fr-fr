---
description: Comment inscrire des filtres DirectShow
ms.assetid: 2b6304c0-4b67-4723-94a0-7b1fff534f91
title: Comment inscrire des filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301f26884115526e25e8875867f7cc2bdc628698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392572"
---
# <a name="how-to-register-directshow-filters"></a><span data-ttu-id="dfa42-103">Comment inscrire des filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="dfa42-103">How to Register DirectShow Filters</span></span>

<span data-ttu-id="dfa42-104">Cet article explique comment effectuer un enregistrement automatique des filtres Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dfa42-104">This article describes how to make a Microsoft DirectShow filter self-registering.</span></span> <span data-ttu-id="dfa42-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="dfa42-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="dfa42-106">Disposition des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="dfa42-106">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
-   [<span data-ttu-id="dfa42-107">Déclaration d’informations de filtre</span><span class="sxs-lookup"><span data-stu-id="dfa42-107">Declaring Filter Information</span></span>](declaring-filter-information.md)
-   [<span data-ttu-id="dfa42-108">Déclaration du modèle de fabrique</span><span class="sxs-lookup"><span data-stu-id="dfa42-108">Declaring the Factory Template</span></span>](declaring-the-factory-template.md)
-   [<span data-ttu-id="dfa42-109">Implémentation de DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="dfa42-109">Implementing DllRegisterServer</span></span>](implementing-dllregisterserver.md)
-   [<span data-ttu-id="dfa42-110">Instructions pour l’enregistrement des filtres</span><span class="sxs-lookup"><span data-stu-id="dfa42-110">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
-   [<span data-ttu-id="dfa42-111">Annulation de l’inscription d’un filtre</span><span class="sxs-lookup"><span data-stu-id="dfa42-111">Unregistering a Filter</span></span>](unregistering-a-filter.md)

<span data-ttu-id="dfa42-112">Cet article ne décrit pas comment créer une DLL pour un filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dfa42-112">This article does not describe how to create a DLL for a DirectShow filter.</span></span> <span data-ttu-id="dfa42-113">Pour plus d’informations sur la création de dll, voir [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="dfa42-113">For information on creating DLLs, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfa42-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfa42-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfa42-115">DirectShow et COM</span><span class="sxs-lookup"><span data-stu-id="dfa42-115">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



