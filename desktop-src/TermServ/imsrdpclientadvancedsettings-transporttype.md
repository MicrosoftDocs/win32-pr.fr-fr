---
title: IMsRdpClientAdvancedSettings propriété TransportType
description: Spécifie le type de transport utilisé par le client.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportType
- Services Bureau à distance de la propriété TransportType, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509294"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="9dfb1-106">IMsRdpClientAdvancedSettings :: TransportType, propriété</span><span class="sxs-lookup"><span data-stu-id="9dfb1-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="9dfb1-107">Spécifie le type de transport utilisé par le client.</span><span class="sxs-lookup"><span data-stu-id="9dfb1-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="9dfb1-108">Cette propriété n’est pas utilisée par le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9dfb1-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="9dfb1-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9dfb1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dfb1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dfb1-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="9dfb1-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9dfb1-111">Property value</span></span>

<span data-ttu-id="9dfb1-112">Définit le type de transport.</span><span class="sxs-lookup"><span data-stu-id="9dfb1-112">Sets the transport type.</span></span> <span data-ttu-id="9dfb1-113">Cette méthode peut être réussie, mais la valeur définie n’est jamais utilisée par le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="9dfb1-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dfb1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9dfb1-114">Remarks</span></span>

<span data-ttu-id="9dfb1-115">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9dfb1-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dfb1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dfb1-116">Requirements</span></span>



| <span data-ttu-id="9dfb1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dfb1-117">Requirement</span></span> | <span data-ttu-id="9dfb1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dfb1-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfb1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dfb1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9dfb1-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dfb1-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9dfb1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dfb1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9dfb1-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dfb1-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9dfb1-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9dfb1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dfb1-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfb1-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9dfb1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9dfb1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dfb1-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dfb1-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9dfb1-127">IID</span><span class="sxs-lookup"><span data-stu-id="9dfb1-127">IID</span></span><br/>                      | <span data-ttu-id="9dfb1-128">IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9dfb1-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dfb1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dfb1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dfb1-130">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9dfb1-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





