---
title: Constantes ADSI
description: Le tableau suivant répertorie les constantes définies et utilisées dans les interfaces de service Active Directory (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671190"
---
# <a name="adsi-constants"></a><span data-ttu-id="9efc5-109">Constantes ADSI</span><span class="sxs-lookup"><span data-stu-id="9efc5-109">ADSI Constants</span></span>

<span data-ttu-id="9efc5-110">Le tableau suivant répertorie les constantes définies et utilisées dans les interfaces de service Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="9efc5-110">The following table lists constants defined and used in Active Directory Service Interfaces (ADSI).</span></span>



| <span data-ttu-id="9efc5-111">Constante ADSI</span><span class="sxs-lookup"><span data-stu-id="9efc5-111">ADSI constant</span></span>                      | <span data-ttu-id="9efc5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9efc5-112">Value</span></span>                                   | <span data-ttu-id="9efc5-113">Description</span><span class="sxs-lookup"><span data-stu-id="9efc5-113">Description</span></span>                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9efc5-114">**\_INITCREDENTIALS ext \_ ads**</span><span class="sxs-lookup"><span data-stu-id="9efc5-114">**ADS\_EXT\_INITCREDENTIALS**</span></span>      | <span data-ttu-id="9efc5-115">1</span><span class="sxs-lookup"><span data-stu-id="9efc5-115">1</span></span>                                       | <span data-ttu-id="9efc5-116">Code de contrôle qui indique que les données personnalisées fournies à la méthode [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contiennent les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9efc5-116">A control code that indicates that the custom data supplied to the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method contains user credentials.</span></span>                                                     |
| <span data-ttu-id="9efc5-117">**\_ \_ initialisation d’AD ext \_ terminée**</span><span class="sxs-lookup"><span data-stu-id="9efc5-117">**ADS\_EXT\_INITIALIZE\_COMPLETE**</span></span> | <span data-ttu-id="9efc5-118">2</span><span class="sxs-lookup"><span data-stu-id="9efc5-118">2</span></span>                                       | <span data-ttu-id="9efc5-119">Code de contrôle utilisé avec [**IADsExtension :: action**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) pour indiquer que les extensions peuvent effectuer toute initialisation nécessaire, en fonction des fonctionnalités prises en charge par l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="9efc5-119">A control code used with [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) to indicate that extensions can perform any necessary initialization, depending on the features supported by the parent object.</span></span> |
| <span data-ttu-id="9efc5-120">**\_MAXEXTDISPID ext \_ ads**</span><span class="sxs-lookup"><span data-stu-id="9efc5-120">**ADS\_EXT\_MAXEXTDISPID**</span></span>         | <span data-ttu-id="9efc5-121">16777215</span><span class="sxs-lookup"><span data-stu-id="9efc5-121">16777215</span></span>                                | <span data-ttu-id="9efc5-122">DISPID le plus élevé qu’un objet d’extension peut utiliser pour ses méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="9efc5-122">The highest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                   |
| <span data-ttu-id="9efc5-123">**\_MINEXTDISPID ext \_ ads**</span><span class="sxs-lookup"><span data-stu-id="9efc5-123">**ADS\_EXT\_MINEXTDISPID**</span></span>         | <span data-ttu-id="9efc5-124">1</span><span class="sxs-lookup"><span data-stu-id="9efc5-124">1</span></span>                                       | <span data-ttu-id="9efc5-125">DISPID le plus bas qu’un objet d’extension peut utiliser pour ses méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="9efc5-125">The lowest DISPID an extension object can use for its methods and properties.</span></span>                                                                                                                                    |
| <span data-ttu-id="9efc5-126">**\_réponse VLV \_ ads**</span><span class="sxs-lookup"><span data-stu-id="9efc5-126">**ADS\_VLV\_RESPONSE**</span></span>             | <span data-ttu-id="9efc5-127">L « fc8cb04d-311D-406c-8CB9-1ae8b843b419 »</span><span class="sxs-lookup"><span data-stu-id="9efc5-127">L"fc8cb04d-311d-406c-8cb9-1ae8b843b419"</span></span> | <span data-ttu-id="9efc5-128">Utilisé avec la méthode [**IDirectorySearch :: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) pour récupérer les métadonnées de recherche VLV.</span><span class="sxs-lookup"><span data-stu-id="9efc5-128">Used with the [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) method to retrieve VLV search metadata.</span></span> <span data-ttu-id="9efc5-129">Pour plus d’informations, consultez [Comment effectuer une recherche à l’aide de VLV](how-to-search-using-vlv.md).</span><span class="sxs-lookup"><span data-stu-id="9efc5-129">For more information, see [How to Search Using VLV](how-to-search-using-vlv.md).</span></span>        |
| <span data-ttu-id="9efc5-130">**DBPROPFLAGS \_ ADSISEARCH**</span><span class="sxs-lookup"><span data-stu-id="9efc5-130">**DBPROPFLAGS\_ADSISEARCH**</span></span>        | <span data-ttu-id="9efc5-131">0x0000C000</span><span class="sxs-lookup"><span data-stu-id="9efc5-131">0x0000C000</span></span>                              | <span data-ttu-id="9efc5-132">Utilisé pour travailler avec le fournisseur de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="9efc5-132">Used to work with the OLE DB provider.</span></span>                                                                                                                                                                           |



 

 

 




