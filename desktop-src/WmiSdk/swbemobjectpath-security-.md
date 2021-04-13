---
description: La propriété de sécurité de l’objet SWbemObjectPath est utilisée pour récupérer ou définir les composants de sécurité d’un chemin d’accès d’objet.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202155"
---
# <a name="swbemobjectpathsecurity_-property"></a><span data-ttu-id="10b18-103">SWbemObjectPath. Security, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="10b18-103">SWbemObjectPath.Security\_ property</span></span>

<span data-ttu-id="10b18-104">La propriété de **sécurité** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) est utilisée pour récupérer ou définir les composants de sécurité d’un chemin d’accès d’objet.</span><span class="sxs-lookup"><span data-stu-id="10b18-104">The **Security** property of the [**SWbemObjectPath**](swbemobjectpath.md) object is used to get or set the security components of an object path.</span></span> <span data-ttu-id="10b18-105">Notez qu’il n’est pas utilisé pour définir des attributs de sécurité de l’objet **SWbemObjectPath** lui-même.</span><span class="sxs-lookup"><span data-stu-id="10b18-105">Note that it is not used to set security attributes of the **SWbemObjectPath** object itself.</span></span> <span data-ttu-id="10b18-106">Il est utilisé uniquement pour représenter les composants de sécurité du chemin d’accès pour un objet [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="10b18-106">It is used only to represent the security components of the path for an [**SWbemLocator**](swbemlocator.md) object.</span></span> <span data-ttu-id="10b18-107">Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="10b18-107">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="10b18-108">La définition de la propriété de [**sécurité \_**](swbemobject-security-.md) d’un objet [**SWbemObjectPath**](swbemobjectset.md) sur la **valeur null** accorde à tout moment un accès illimité à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="10b18-108">Setting the [**Security\_**](swbemobject-security-.md) property of an [**SWbemObjectPath**](swbemobjectset.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="10b18-109">Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="10b18-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="10b18-110">Pour plus d’informations, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="10b18-110">For more information, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="10b18-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="10b18-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b18-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10b18-112">Syntax</span></span>


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="10b18-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="10b18-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="10b18-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10b18-114">Requirements</span></span>



| <span data-ttu-id="10b18-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10b18-115">Requirement</span></span> | <span data-ttu-id="10b18-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="10b18-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b18-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b18-117">Minimum supported client</span></span><br/> | <span data-ttu-id="10b18-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10b18-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10b18-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10b18-119">Minimum supported server</span></span><br/> | <span data-ttu-id="10b18-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10b18-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10b18-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="10b18-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b18-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b18-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="10b18-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="10b18-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="10b18-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="10b18-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="10b18-125">DLL</span><span class="sxs-lookup"><span data-stu-id="10b18-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10b18-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10b18-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="10b18-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="10b18-127">CLSID</span></span><br/>                    | <span data-ttu-id="10b18-128">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="10b18-128">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="10b18-129">IID</span><span class="sxs-lookup"><span data-stu-id="10b18-129">IID</span></span><br/>                      | <span data-ttu-id="10b18-130">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="10b18-130">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="10b18-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10b18-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b18-132">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="10b18-132">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> <dt>

[<span data-ttu-id="10b18-133">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="10b18-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="10b18-134">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="10b18-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> </dl>

 

 




