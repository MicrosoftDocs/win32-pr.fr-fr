---
description: Le message CREATEDIALOGINSTANCE de la ligne TSPI fait en sorte que l' \_ interface TAPI crée une association entre le fournisseur de services et une instance de la \_ fonction TUISPI providerGenericDialog s’exécutant dans le contexte de l’application.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Message LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532866"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="6d8e5-103">\_Message CREATEDIALOGINSTANCE de ligne</span><span class="sxs-lookup"><span data-stu-id="6d8e5-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="6d8e5-104">Le message **\_ CREATEDIALOGINSTANCE** de la ligne TSPI fait que l’interface TAPI crée une association entre le fournisseur de services et une instance de la fonction [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) s’exécutant dans le contexte de l’application qui a appelé la fonction TSPI asynchrone identifiée par le paramètre *DwRequestID* de la structure [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) désignée par *lpTUISPICreateDialogInstanceParams*.</span><span class="sxs-lookup"><span data-stu-id="6d8e5-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6d8e5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d8e5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8e5-106">*hProvider*</span><span class="sxs-lookup"><span data-stu-id="6d8e5-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8e5-107">ProviderHandle fourni au fournisseur de services en tant que paramètre pour [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span><span class="sxs-lookup"><span data-stu-id="6d8e5-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="6d8e5-108">*lpTUISPICreateDialogInstanceParams*</span><span class="sxs-lookup"><span data-stu-id="6d8e5-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="6d8e5-109">Pointeur vers une structure [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .</span><span class="sxs-lookup"><span data-stu-id="6d8e5-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d8e5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d8e5-110">Requirements</span></span>



| <span data-ttu-id="6d8e5-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d8e5-111">Requirement</span></span> | <span data-ttu-id="6d8e5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d8e5-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d8e5-113">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6d8e5-113">TAPI version</span></span><br/> | <span data-ttu-id="6d8e5-114">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6d8e5-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6d8e5-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d8e5-115">Header</span></span><br/>       | <dl> <span data-ttu-id="6d8e5-116"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d8e5-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8e5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d8e5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8e5-118">**TSPI \_ providerEnumDevices**</span><span class="sxs-lookup"><span data-stu-id="6d8e5-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="6d8e5-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="6d8e5-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

