---
title: IMsRdpClientShell propriété RdpFileContents
description: Spécifie ou récupère le contenu du fichier protocole RDP (Remote Desktop Protocol) (RDP) à lancer à partir d’Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RdpFileContents
- Services Bureau à distance de la propriété RdpFileContents, interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, propriété RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509932"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="fb44d-106">IMsRdpClientShell :: RdpFileContents, propriété</span><span class="sxs-lookup"><span data-stu-id="fb44d-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="fb44d-107">Spécifie ou récupère le contenu du fichier protocole RDP (Remote Desktop Protocol) (RDP) à lancer à partir d’Bureau à distance Accès web (RD Accès web) ou d’un autre portail Web.</span><span class="sxs-lookup"><span data-stu-id="fb44d-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="fb44d-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fb44d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb44d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb44d-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="fb44d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb44d-110">Property value</span></span>

<span data-ttu-id="fb44d-111">Spécifie le contenu du fichier RDP à lancer à partir du portail Web.</span><span class="sxs-lookup"><span data-stu-id="fb44d-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb44d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb44d-112">Requirements</span></span>



| <span data-ttu-id="fb44d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb44d-113">Requirement</span></span> | <span data-ttu-id="fb44d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb44d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb44d-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb44d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fb44d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb44d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fb44d-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb44d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fb44d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb44d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fb44d-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fb44d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb44d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb44d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb44d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fb44d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb44d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb44d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb44d-123">IID</span><span class="sxs-lookup"><span data-stu-id="fb44d-123">IID</span></span><br/>                      | <span data-ttu-id="fb44d-124">IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="fb44d-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="fb44d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb44d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb44d-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="fb44d-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





