---
title: Propriété IMsRdpClientAdvancedSettings6 PCB
description: Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur. | Propriété IMsRdpClientAdvancedSettings6 PCB
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété PCB
- Services Bureau à distance de propriété PCB, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété PCB
- Services Bureau à distance de propriété PCB, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété PCB
- Services Bureau à distance de propriété PCB, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété PCB
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538042"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="22ac5-111">IMsRdpClientAdvancedSettings6 ::P propriété CB</span><span class="sxs-lookup"><span data-stu-id="22ac5-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="22ac5-112">Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur.</span><span class="sxs-lookup"><span data-stu-id="22ac5-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="22ac5-113">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="22ac5-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ac5-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22ac5-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="22ac5-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="22ac5-115">Property value</span></span>

<span data-ttu-id="22ac5-116">Spécifie le paramètre d’objet BLOB à utiliser avant la connexion.</span><span class="sxs-lookup"><span data-stu-id="22ac5-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ac5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="22ac5-117">Remarks</span></span>

<span data-ttu-id="22ac5-118">Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.</span><span class="sxs-lookup"><span data-stu-id="22ac5-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="22ac5-119">Le serveur utilise le paramètre BLOB pour identifier le processus cible de la connexion.</span><span class="sxs-lookup"><span data-stu-id="22ac5-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ac5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22ac5-120">Requirements</span></span>



| <span data-ttu-id="22ac5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22ac5-121">Requirement</span></span> | <span data-ttu-id="22ac5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="22ac5-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ac5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ac5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22ac5-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22ac5-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="22ac5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ac5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22ac5-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="22ac5-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="22ac5-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="22ac5-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="22ac5-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ac5-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="22ac5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="22ac5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ac5-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ac5-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="22ac5-131">IID</span><span class="sxs-lookup"><span data-stu-id="22ac5-131">IID</span></span><br/>                      | <span data-ttu-id="22ac5-132">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="22ac5-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22ac5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22ac5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ac5-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="22ac5-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="22ac5-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="22ac5-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="22ac5-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="22ac5-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





