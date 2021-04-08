---
title: IMsRdpClientAdvancedSettings8 propriété ClientProtocolSpec
description: Spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ClientProtocolSpec
- Services Bureau à distance de la propriété ClientProtocolSpec, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ClientProtocolSpec
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941813"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="96409-106">IMsRdpClientAdvancedSettings8 :: ClientProtocolSpec, propriété</span><span class="sxs-lookup"><span data-stu-id="96409-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="96409-107">Spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="96409-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="96409-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="96409-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="96409-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96409-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="96409-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="96409-110">Property value</span></span>

<span data-ttu-id="96409-111">Valeur de l’énumération [**ClientSpec**](clientspec.md) qui spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="96409-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="96409-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96409-112">Requirements</span></span>



| <span data-ttu-id="96409-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96409-113">Requirement</span></span> | <span data-ttu-id="96409-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="96409-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96409-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96409-115">Minimum supported client</span></span><br/> | <span data-ttu-id="96409-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="96409-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="96409-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96409-117">Minimum supported server</span></span><br/> | <span data-ttu-id="96409-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="96409-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="96409-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="96409-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="96409-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96409-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="96409-121">DLL</span><span class="sxs-lookup"><span data-stu-id="96409-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96409-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96409-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96409-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96409-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96409-124">**ClientSpec**</span><span class="sxs-lookup"><span data-stu-id="96409-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="96409-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="96409-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





