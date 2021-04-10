---
description: Implémente les interfaces IAxiService et IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Objet CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951255"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="9b6ff-103">Objet CIeAxiInstallerService</span><span class="sxs-lookup"><span data-stu-id="9b6ff-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="9b6ff-104">L’objet **CIeAxiInstallerService** implémente les interfaces [**IAxiService**](ieaxiservice.md) et [**IeAxiServiceCallback**](ieaxiservicecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="9b6ff-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="9b6ff-105">Cet objet n’est pas déclaré dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="9b6ff-105">This object is not declared in a public header.</span></span> <span data-ttu-id="9b6ff-106">Les applications doivent les définir elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="9b6ff-106">Applications must define it themselves.</span></span> <span data-ttu-id="9b6ff-107">Le fragment IDL (Interface Definition Language) suivant décrit cet objet, y compris son CLSID.</span><span class="sxs-lookup"><span data-stu-id="9b6ff-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="9b6ff-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b6ff-108">Requirements</span></span>



| <span data-ttu-id="9b6ff-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b6ff-109">Requirement</span></span> | <span data-ttu-id="9b6ff-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b6ff-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6ff-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6ff-111">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6ff-112">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b6ff-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9b6ff-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6ff-113">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6ff-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b6ff-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="9b6ff-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b6ff-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6ff-116">**IAxiService**</span><span class="sxs-lookup"><span data-stu-id="9b6ff-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="9b6ff-117">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="9b6ff-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




