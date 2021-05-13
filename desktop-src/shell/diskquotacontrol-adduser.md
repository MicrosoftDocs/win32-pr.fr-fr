---
description: Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.
title: DiskQuotaControl. AddUser, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: 9dd69b78210ecda418e784681694d84b27b1732a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841530"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="e7d34-103">DiskQuotaControl. AddUser, méthode</span><span class="sxs-lookup"><span data-stu-id="e7d34-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="e7d34-104">Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7d34-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d34-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="e7d34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d34-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="e7d34-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="e7d34-108">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="e7d34-108">Type: **CHAR**</span></span>

<span data-ttu-id="e7d34-109">Valeur de chaîne qui contient le nom d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7d34-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="e7d34-110">Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour spécifier la façon dont le nom doit être résolu.</span><span class="sxs-lookup"><span data-stu-id="e7d34-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d34-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7d34-111">Return value</span></span>

<span data-ttu-id="e7d34-112">Type : **Object**</span><span class="sxs-lookup"><span data-stu-id="e7d34-112">Type: **Object**</span></span>

<span data-ttu-id="e7d34-113">Retourne une expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7d34-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d34-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d34-114">Remarks</span></span>

<span data-ttu-id="e7d34-115">Le système de fichiers NTFS crée automatiquement une entrée de quota utilisateur lorsqu’un utilisateur écrit pour la première fois sur le volume.</span><span class="sxs-lookup"><span data-stu-id="e7d34-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="e7d34-116">Les entrées créées de cette façon reçoivent le seuil d’avertissement par défaut et les valeurs de limite de quota matériel pour le volume.</span><span class="sxs-lookup"><span data-stu-id="e7d34-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="e7d34-117">Cette méthode vous permet de créer une entrée de quota utilisateur avant qu’un utilisateur n’écrive des informations sur le volume.</span><span class="sxs-lookup"><span data-stu-id="e7d34-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="e7d34-118">Elle retourne un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) qui peut être utilisé pour assigner une valeur de seuil d’avertissement ou de limite de quota différente des paramètres par défaut du volume.</span><span class="sxs-lookup"><span data-stu-id="e7d34-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="e7d34-119">Si l’utilisateur existe déjà, aucune nouvelle entrée n’est créée.</span><span class="sxs-lookup"><span data-stu-id="e7d34-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="e7d34-120">La méthode retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) associé à l’entrée existante.</span><span class="sxs-lookup"><span data-stu-id="e7d34-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d34-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7d34-121">Requirements</span></span>



| <span data-ttu-id="e7d34-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7d34-122">Requirement</span></span> | <span data-ttu-id="e7d34-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7d34-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d34-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d34-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d34-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7d34-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7d34-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7d34-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d34-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7d34-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e7d34-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d34-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7d34-129"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e7d34-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d34-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d34-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d34-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="e7d34-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="e7d34-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="e7d34-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="e7d34-133">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="e7d34-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




