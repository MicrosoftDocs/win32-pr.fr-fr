---
description: Appelée par l’interface IeAxiSystemInstaller pour vérifier qu’un objet ActiveX peut être installé.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interface IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869025"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="495bd-103">Interface IeAxiServiceCallback</span><span class="sxs-lookup"><span data-stu-id="495bd-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="495bd-104">L’interface **IeAxiServiceCallback** est appelée par l’interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) pour vérifier qu’un objet ActiveX peut être installé.</span><span class="sxs-lookup"><span data-stu-id="495bd-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="495bd-105">La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="495bd-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="495bd-106">Cette interface n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="495bd-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="495bd-107">Les applications doivent les définir elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="495bd-107">Applications must define it themselves.</span></span> <span data-ttu-id="495bd-108">Le fragment IDL (Interface Definition Language) suivant décrit cette interface, y compris son IID.</span><span class="sxs-lookup"><span data-stu-id="495bd-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="495bd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="495bd-109">Members</span></span>

<span data-ttu-id="495bd-110">L’interface **IeAxiServiceCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="495bd-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="495bd-111">**IeAxiServiceCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="495bd-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="495bd-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="495bd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="495bd-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="495bd-113">Methods</span></span>

<span data-ttu-id="495bd-114">L’interface **IeAxiServiceCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="495bd-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="495bd-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="495bd-115">Method</span></span>                                                | <span data-ttu-id="495bd-116">Description</span><span class="sxs-lookup"><span data-stu-id="495bd-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="495bd-117">**VerifyFile**</span><span class="sxs-lookup"><span data-stu-id="495bd-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="495bd-118">Effectue des vérifications de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier. cab correspondant a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="495bd-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="495bd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="495bd-119">Requirements</span></span>



| <span data-ttu-id="495bd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="495bd-120">Requirement</span></span> | <span data-ttu-id="495bd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="495bd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495bd-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="495bd-123">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="495bd-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="495bd-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="495bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="495bd-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="495bd-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="495bd-126">IID</span><span class="sxs-lookup"><span data-stu-id="495bd-126">IID</span></span><br/>                      | <span data-ttu-id="495bd-127">IID \_ IeAxiServiceCallback est défini en tant que 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="495bd-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

