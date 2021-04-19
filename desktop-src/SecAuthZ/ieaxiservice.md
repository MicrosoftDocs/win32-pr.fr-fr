---
description: Initialise un objet de service système pour installer un objet ActiveX lorsque l’utilisateur actuel n’est pas autorisé à installer l’objet.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interface IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529333"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="67922-103">Interface IeAxiService</span><span class="sxs-lookup"><span data-stu-id="67922-103">IeAxiService interface</span></span>

<span data-ttu-id="67922-104">L’interface **IAxiService** Initialise un objet de service système pour installer un objet ActiveX lorsque l’utilisateur actuel n’est pas autorisé à installer l’objet.</span><span class="sxs-lookup"><span data-stu-id="67922-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="67922-105">La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="67922-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="67922-106">Cette interface n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="67922-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="67922-107">Les applications doivent les définir elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="67922-107">Applications must define it themselves.</span></span> <span data-ttu-id="67922-108">Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.</span><span class="sxs-lookup"><span data-stu-id="67922-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="67922-109">Membres</span><span class="sxs-lookup"><span data-stu-id="67922-109">Members</span></span>

<span data-ttu-id="67922-110">L’interface **IeAxiService** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="67922-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67922-111">**IeAxiService** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67922-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="67922-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67922-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67922-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67922-113">Methods</span></span>

<span data-ttu-id="67922-114">L’interface **IeAxiService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="67922-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="67922-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="67922-115">Method</span></span>                                        | <span data-ttu-id="67922-116">Description</span><span class="sxs-lookup"><span data-stu-id="67922-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="67922-117">**Nettoyage**</span><span class="sxs-lookup"><span data-stu-id="67922-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="67922-118">Libère les ressources utilisées par l’interface **IeAxiService** .</span><span class="sxs-lookup"><span data-stu-id="67922-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="67922-119">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="67922-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="67922-120">Vérifie et télécharge un objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="67922-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="67922-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67922-121">Requirements</span></span>



| <span data-ttu-id="67922-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67922-122">Requirement</span></span> | <span data-ttu-id="67922-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="67922-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67922-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67922-124">Minimum supported client</span></span><br/> | <span data-ttu-id="67922-125">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67922-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="67922-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67922-126">Minimum supported server</span></span><br/> | <span data-ttu-id="67922-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="67922-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="67922-128">IID</span><span class="sxs-lookup"><span data-stu-id="67922-128">IID</span></span><br/>                      | <span data-ttu-id="67922-129">IID \_ IeAxiService est défini en tant que E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="67922-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

