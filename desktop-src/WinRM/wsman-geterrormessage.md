---
title: Méthode WSMan. GetErrorMessage (WSManDisp. h)
description: Retourne une chaîne mise en forme qui contient le texte d’un numéro d’erreur.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode GetErrorMessage
- Méthode GetErrorMessage Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317254"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="b08f4-106">Méthode WSMan. GetErrorMessage</span><span class="sxs-lookup"><span data-stu-id="b08f4-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="b08f4-107">Retourne une chaîne mise en forme qui contient le texte d’un numéro d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b08f4-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="b08f4-108">Cette méthode effectue la même opération que le numéro d’erreur **de ligne de commande WinRM** **WinRM** *ou hexadécimal*.</span><span class="sxs-lookup"><span data-stu-id="b08f4-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08f4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b08f4-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="b08f4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b08f4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08f4-111">*errornumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b08f4-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08f4-112">Numéro de message d’erreur au format décimal ou hexadécimal de WinRM, WinHTTP ou d’autres composants du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b08f4-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="b08f4-113">*ErrorMessage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b08f4-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b08f4-114">Chaîne de message d’erreur mise en forme comme les messages retournés par la commande **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="b08f4-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b08f4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b08f4-115">Remarks</span></span>

<span data-ttu-id="b08f4-116">La méthode C++ correspondante est [**IWSManEx :: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span><span class="sxs-lookup"><span data-stu-id="b08f4-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="b08f4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b08f4-117">Requirements</span></span>



| <span data-ttu-id="b08f4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b08f4-118">Requirement</span></span> | <span data-ttu-id="b08f4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b08f4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08f4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b08f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b08f4-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b08f4-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b08f4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b08f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b08f4-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b08f4-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b08f4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b08f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b08f4-125"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b08f4-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b08f4-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="b08f4-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b08f4-127"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b08f4-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b08f4-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b08f4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b08f4-129"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b08f4-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b08f4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b08f4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b08f4-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b08f4-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b08f4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b08f4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08f4-133">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="b08f4-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





