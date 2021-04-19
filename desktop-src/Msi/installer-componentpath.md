---
description: La propriété ComponentPath est une propriété en lecture seule qui retourne le chemin d’accès complet à un composant installé. Si le chemin d’accès à la clé du composant est une clé de Registre, la clé de Registre est retournée.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer. ComponentPath, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541288"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="f8a71-104">Installer. ComponentPath, propriété</span><span class="sxs-lookup"><span data-stu-id="f8a71-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="f8a71-105">La propriété **ComponentPath** est une propriété en lecture seule qui retourne le chemin d’accès complet à un composant installé.</span><span class="sxs-lookup"><span data-stu-id="f8a71-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="f8a71-106">Si le chemin d’accès à la clé du composant est une clé de Registre, la clé de Registre est retournée.</span><span class="sxs-lookup"><span data-stu-id="f8a71-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="f8a71-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f8a71-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8a71-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="f8a71-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f8a71-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a71-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f8a71-110">Remarks</span></span>

<span data-ttu-id="f8a71-111">Si le composant est une clé de Registre, les racines du Registre sont représentées par ordre numérique.</span><span class="sxs-lookup"><span data-stu-id="f8a71-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="f8a71-112">Par exemple, le chemin d’accès au registre « HKEY \_ Current \_ User \\ Software \\ Microsoft » est retourné sous la forme « 01 : \\ Software \\ Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="f8a71-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="f8a71-113">Les racines de Registre retournées sont définies comme suit :</span><span class="sxs-lookup"><span data-stu-id="f8a71-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="f8a71-114">Root</span><span class="sxs-lookup"><span data-stu-id="f8a71-114">Root</span></span>                    | <span data-ttu-id="f8a71-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8a71-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="f8a71-116">\_racine des classes HKEY \_</span><span class="sxs-lookup"><span data-stu-id="f8a71-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="f8a71-117">00</span><span class="sxs-lookup"><span data-stu-id="f8a71-117">00</span></span>             |
| <span data-ttu-id="f8a71-118">HKEY \_ Current \_ User</span><span class="sxs-lookup"><span data-stu-id="f8a71-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="f8a71-119">01</span><span class="sxs-lookup"><span data-stu-id="f8a71-119">01</span></span>             |
| <span data-ttu-id="f8a71-120">HKEY \_ local \_ machine</span><span class="sxs-lookup"><span data-stu-id="f8a71-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="f8a71-121">02</span><span class="sxs-lookup"><span data-stu-id="f8a71-121">02</span></span>             |
| <span data-ttu-id="f8a71-122">HKEY, \_ utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f8a71-122">HKEY\_USERS</span></span>             | <span data-ttu-id="f8a71-123">03</span><span class="sxs-lookup"><span data-stu-id="f8a71-123">03</span></span>             |
| <span data-ttu-id="f8a71-124">\_données de performances HKEY \_</span><span class="sxs-lookup"><span data-stu-id="f8a71-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="f8a71-125">04</span><span class="sxs-lookup"><span data-stu-id="f8a71-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="f8a71-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8a71-126">Requirements</span></span>



| <span data-ttu-id="f8a71-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8a71-127">Requirement</span></span> | <span data-ttu-id="f8a71-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8a71-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a71-129">Version</span><span class="sxs-lookup"><span data-stu-id="f8a71-129">Version</span></span><br/> | <span data-ttu-id="f8a71-130">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8a71-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8a71-131">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8a71-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8a71-132">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8a71-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f8a71-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a71-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8a71-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8a71-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f8a71-135">IID</span><span class="sxs-lookup"><span data-stu-id="f8a71-135">IID</span></span><br/>     | <span data-ttu-id="f8a71-136">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f8a71-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f8a71-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8a71-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a71-138">**MsiGetComponentPath**</span><span class="sxs-lookup"><span data-stu-id="f8a71-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




