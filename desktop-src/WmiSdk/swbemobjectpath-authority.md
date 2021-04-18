---
description: La propriété Authority de l’objet SWbemObjectPath contient une chaîne qui définit le composant d’autorité du chemin d’accès de l’objet.
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: Propriété SWbemObjectPath. Authority (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519552"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="da0d3-103">SWbemObjectPath. Authority, propriété</span><span class="sxs-lookup"><span data-stu-id="da0d3-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="da0d3-104">La propriété **Authority** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient une chaîne qui définit le composant d’autorité du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="da0d3-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="da0d3-105">Pour plus d’informations, consultez le paramètre *strAuthority* de la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) et [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="da0d3-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="da0d3-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="da0d3-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="da0d3-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="da0d3-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0d3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da0d3-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="da0d3-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="da0d3-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="da0d3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da0d3-110">Requirements</span></span>



| <span data-ttu-id="da0d3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da0d3-111">Requirement</span></span> | <span data-ttu-id="da0d3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="da0d3-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0d3-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da0d3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="da0d3-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da0d3-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da0d3-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da0d3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="da0d3-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da0d3-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da0d3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="da0d3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="da0d3-118"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="da0d3-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="da0d3-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="da0d3-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="da0d3-120"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da0d3-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da0d3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="da0d3-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da0d3-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da0d3-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="da0d3-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="da0d3-123">CLSID</span></span><br/>                    | <span data-ttu-id="da0d3-124">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="da0d3-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="da0d3-125">IID</span><span class="sxs-lookup"><span data-stu-id="da0d3-125">IID</span></span><br/>                      | <span data-ttu-id="da0d3-126">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="da0d3-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




