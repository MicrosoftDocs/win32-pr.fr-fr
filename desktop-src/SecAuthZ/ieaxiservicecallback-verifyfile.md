---
description: Effectue des vérifications de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier. cab correspondant a été téléchargé.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'IeAxiServiceCallback :: VerifyFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529878"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a><span data-ttu-id="833c0-103">IeAxiServiceCallback :: VerifyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="833c0-103">IeAxiServiceCallback::VerifyFile method</span></span>

<span data-ttu-id="833c0-104">La méthode **VerifyFile** effectue des contrôles de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier. cab correspondant a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="833c0-104">The **VerifyFile** method performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span>

## <a name="syntax"></a><span data-ttu-id="833c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833c0-105">Syntax</span></span>


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a><span data-ttu-id="833c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833c0-107">*bstrFileUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="833c0-107">*bstrFileUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833c0-108">URL de l’objet ActiveX à vérifier.</span><span class="sxs-lookup"><span data-stu-id="833c0-108">The URL of the ActiveX object to check.</span></span>

</dd> <dt>

<span data-ttu-id="833c0-109">*bstrApprovedFileName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="833c0-109">*bstrApprovedFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="833c0-110">Nom du fichier dans lequel le fichier. cab associé à l’objet ActiveX a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="833c0-110">The name of the file where the .cab file associated with the ActiveX object was downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833c0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="833c0-111">Return value</span></span>

<span data-ttu-id="833c0-112">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="833c0-112">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="833c0-113">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="833c0-113">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="833c0-114">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="833c0-114">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="833c0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="833c0-115">Requirements</span></span>



| <span data-ttu-id="833c0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="833c0-116">Requirement</span></span> | <span data-ttu-id="833c0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="833c0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="833c0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="833c0-119">Windows Vista Professionnel, Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="833c0-119">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="833c0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="833c0-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="833c0-121">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="833c0-122">IID</span><span class="sxs-lookup"><span data-stu-id="833c0-122">IID</span></span><br/>                      | <span data-ttu-id="833c0-123">IID \_ IeAxiServiceCallback est défini en tant que 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="833c0-123">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="833c0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833c0-125">**IeAxiServiceCallback**</span><span class="sxs-lookup"><span data-stu-id="833c0-125">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

