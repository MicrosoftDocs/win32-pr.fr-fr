---
title: IMsRdpClientNonScriptable5 propriété RemoteMonitorLayoutMatchesLocal
description: Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteMonitorLayoutMatchesLocal
- Services Bureau à distance de la propriété RemoteMonitorLayoutMatchesLocal, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104620"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="f7c91-106">IMsRdpClientNonScriptable5 :: RemoteMonitorLayoutMatchesLocal, propriété</span><span class="sxs-lookup"><span data-stu-id="f7c91-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="f7c91-107">Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local.</span><span class="sxs-lookup"><span data-stu-id="f7c91-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="f7c91-108">Si cette propriété contient **la \_ valeur true**, la disposition du moniteur distant est identique à la disposition du moniteur local.</span><span class="sxs-lookup"><span data-stu-id="f7c91-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="f7c91-109">Si cette propriété contient **la \_ valeur false**, les analyses locales et distantes ont des dispositions différentes.</span><span class="sxs-lookup"><span data-stu-id="f7c91-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="f7c91-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f7c91-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c91-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7c91-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="f7c91-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f7c91-112">Property value</span></span>

<span data-ttu-id="f7c91-113">Reçoit la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="f7c91-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c91-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7c91-114">Requirements</span></span>



| <span data-ttu-id="f7c91-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7c91-115">Requirement</span></span> | <span data-ttu-id="f7c91-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7c91-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c91-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c91-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c91-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7c91-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7c91-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7c91-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c91-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7c91-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="f7c91-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7c91-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7c91-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c91-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="f7c91-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f7c91-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c91-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c91-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="f7c91-125">IID</span><span class="sxs-lookup"><span data-stu-id="f7c91-125">IID</span></span><br/>                      | <span data-ttu-id="f7c91-126">IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="f7c91-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7c91-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7c91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c91-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="f7c91-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





