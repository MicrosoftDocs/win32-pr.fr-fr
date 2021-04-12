---
title: Obtention des propriétés de gestion des comptes
description: L’objet Accounting est l’un des objets de la collection de gestionnaires de demandes.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382235"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="5e64a-103">Obtention des propriétés de gestion des comptes</span><span class="sxs-lookup"><span data-stu-id="5e64a-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="5e64a-104">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5e64a-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="5e64a-105">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="5e64a-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="5e64a-106">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="5e64a-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="5e64a-107">L’objet Accounting est l’un des objets de la collection de gestionnaires de demandes.</span><span class="sxs-lookup"><span data-stu-id="5e64a-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="5e64a-108">La valeur d’énumération pour la collection de gestionnaires de demandes est la propriété de la **\_ \_ \_ collection REQUESTHANDLERS IAS**.</span><span class="sxs-lookup"><span data-stu-id="5e64a-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="5e64a-109">Le nom du gestionnaire de l’objet de gestion des comptes est « Microsoft Accounting ».</span><span class="sxs-lookup"><span data-stu-id="5e64a-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="5e64a-110">Le code Visual Basic suivant accède aux propriétés disponibles à partir du gestionnaire d’objets de comptabilité.</span><span class="sxs-lookup"><span data-stu-id="5e64a-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="5e64a-111">Pour accéder aux propriétés de gestion de comptes à l’aide de C++, obtenez d’abord la collection de gestionnaires de demandes.</span><span class="sxs-lookup"><span data-stu-id="5e64a-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="5e64a-112">La [récupération d’une collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contient du code C++ qui montre comment obtenir une collection.</span><span class="sxs-lookup"><span data-stu-id="5e64a-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="5e64a-113">La valeur d’énumération pour la collection de gestionnaires de demandes est la propriété de la **\_ \_ \_ collection REQUESTHANDLERS IAS**.</span><span class="sxs-lookup"><span data-stu-id="5e64a-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="5e64a-114">(Les valeurs correspondant aux différentes collections NPS sont énumérées par le type d’énumération [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)</span><span class="sxs-lookup"><span data-stu-id="5e64a-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="5e64a-115">La collection de gestionnaires de demandes contient un objet nommé « Microsoft Accounting ».</span><span class="sxs-lookup"><span data-stu-id="5e64a-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="5e64a-116">Récupérez cet objet de la collection.</span><span class="sxs-lookup"><span data-stu-id="5e64a-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="5e64a-117">La section [récupération d’un objet d’une collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contient du code C++ qui montre comment obtenir un objet à partir d’une collection.</span><span class="sxs-lookup"><span data-stu-id="5e64a-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="5e64a-118">Une fois que vous disposez de l’objet Microsoft Accounting, obtenez une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) pour l’objet à l’aide de [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="5e64a-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="5e64a-119">La section [récupération d’un utilisateur SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contient du code C++ qui montre comment obtenir une interface **ISdo** pour un objet.</span><span class="sxs-lookup"><span data-stu-id="5e64a-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="5e64a-120">Vous pouvez ensuite utiliser la méthode [**ISdo :: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) pour obtenir les valeurs de propriété de l’objet Microsoft Accounting.</span><span class="sxs-lookup"><span data-stu-id="5e64a-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e64a-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e64a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e64a-122">Récupération d’une collection</span><span class="sxs-lookup"><span data-stu-id="5e64a-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="5e64a-123">Récupération d’un objet à partir d’une collection</span><span class="sxs-lookup"><span data-stu-id="5e64a-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="5e64a-124">Récupération d’un utilisateur SDO</span><span class="sxs-lookup"><span data-stu-id="5e64a-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="5e64a-125">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="5e64a-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="5e64a-126">[**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="5e64a-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="5e64a-127">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="5e64a-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 