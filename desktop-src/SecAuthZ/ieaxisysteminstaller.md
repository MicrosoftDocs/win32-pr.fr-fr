---
description: Installe un objet ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interface IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035115"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="d8949-103">Interface IeAxiSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="d8949-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="d8949-104">L’interface **IeAxiSystemInstaller** installe un objet ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d8949-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="d8949-105">Cette interface n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="d8949-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="d8949-106">Les applications doivent les définir elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="d8949-106">Applications must define it themselves.</span></span> <span data-ttu-id="d8949-107">Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.</span><span class="sxs-lookup"><span data-stu-id="d8949-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="d8949-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d8949-108">Members</span></span>

<span data-ttu-id="d8949-109">L’interface **IeAxiSystemInstaller** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d8949-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d8949-110">**IeAxiSystemInstaller** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8949-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="d8949-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8949-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8949-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8949-112">Methods</span></span>

<span data-ttu-id="d8949-113">L’interface **IeAxiSystemInstaller** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d8949-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="d8949-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="d8949-114">Method</span></span>                                                                              | <span data-ttu-id="d8949-115">Description</span><span class="sxs-lookup"><span data-stu-id="d8949-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="d8949-116">**InitializeSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="d8949-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="d8949-117">Installe l’objet ActiveX spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8949-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8949-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8949-118">Requirements</span></span>



| <span data-ttu-id="d8949-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8949-119">Requirement</span></span> | <span data-ttu-id="d8949-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8949-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8949-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8949-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8949-122">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8949-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8949-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8949-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8949-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8949-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="d8949-125">IID</span><span class="sxs-lookup"><span data-stu-id="d8949-125">IID</span></span><br/>                      | <span data-ttu-id="d8949-126">IID \_ IeAxiSystemInstaller est défini en tant que a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="d8949-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

