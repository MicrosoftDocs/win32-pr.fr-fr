---
description: La \_ propriété de sécurité de l’objet SWbemObjectSet est utilisée pour obtenir ou définir les paramètres de sécurité d’un objet SWbemObjectSet. Cette propriété est un objet SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534429"
---
# <a name="swbemobjectsetsecurity_-property"></a><span data-ttu-id="a9b88-104">Propriété SWbemObjectSet. Security \_</span><span class="sxs-lookup"><span data-stu-id="a9b88-104">SWbemObjectSet.Security\_ property</span></span>

<span data-ttu-id="a9b88-105">La propriété de **\_ sécurité** de l’objet [**SWbemObjectSet**](swbemobjectset.md) est utilisée pour obtenir ou définir les paramètres de sécurité d’un objet **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="a9b88-105">The **Security\_** property of the [**SWbemObjectSet**](swbemobjectset.md) object is used to get or set the security settings for an **SWbemObjectSet** object.</span></span> <span data-ttu-id="a9b88-106">Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="a9b88-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="a9b88-107">La définition de la propriété de [**\_ sécurité**](swbemobject-security-.md) d’un objet [**SWbemObjectSet**](swbemobjectset.md) sur **null** accorde à tout moment un accès illimité à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a9b88-107">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectSet**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="a9b88-108">Pour plus d’informations sur les implications d’un accès illimité, consultez [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="a9b88-108">For more information about the implications of unlimited access, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="a9b88-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a9b88-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a9b88-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a9b88-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9b88-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9b88-111">Syntax</span></span>


```VB
SWbemObjectSet.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="a9b88-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a9b88-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b88-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9b88-113">Requirements</span></span>



| <span data-ttu-id="a9b88-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9b88-114">Requirement</span></span> | <span data-ttu-id="a9b88-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9b88-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b88-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b88-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b88-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9b88-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9b88-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9b88-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b88-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9b88-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9b88-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9b88-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b88-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9b88-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9b88-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a9b88-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9b88-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a9b88-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a9b88-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a9b88-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9b88-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9b88-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9b88-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="a9b88-126">CLSID</span></span><br/>                    | <span data-ttu-id="a9b88-127">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9b88-127">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="a9b88-128">IID</span><span class="sxs-lookup"><span data-stu-id="a9b88-128">IID</span></span><br/>                      | <span data-ttu-id="a9b88-129">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9b88-129">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="a9b88-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9b88-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b88-131">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="a9b88-131">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="a9b88-132">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="a9b88-132">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="a9b88-133">Sécurisation des clients de script</span><span class="sxs-lookup"><span data-stu-id="a9b88-133">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

 




