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
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525336"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="4e1cd-103">DiskQuotaControl. AddUser, méthode</span><span class="sxs-lookup"><span data-stu-id="4e1cd-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="4e1cd-104">Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e1cd-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="4e1cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e1cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1cd-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="4e1cd-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="4e1cd-108">Type : **char**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-108">Type: **CHAR**</span></span>

<span data-ttu-id="4e1cd-109">Valeur de chaîne qui contient le nom d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="4e1cd-110">Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour spécifier la façon dont le nom doit être résolu.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1cd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e1cd-111">Return value</span></span>

<span data-ttu-id="4e1cd-112">Type : **Object**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-112">Type: **Object**</span></span>

<span data-ttu-id="4e1cd-113">Retourne une expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1cd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4e1cd-114">Remarks</span></span>

<span data-ttu-id="4e1cd-115">Le système de fichiers NTFS crée automatiquement une entrée de quota utilisateur lorsqu’un utilisateur écrit pour la première fois sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="4e1cd-116">Les entrées créées de cette façon reçoivent le seuil d’avertissement par défaut et les valeurs de limite de quota matériel pour le volume.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="4e1cd-117">Cette méthode vous permet de créer une entrée de quota utilisateur avant qu’un utilisateur n’écrive des informations sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="4e1cd-118">Elle retourne un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) qui peut être utilisé pour assigner une valeur de seuil d’avertissement ou de limite de quota différente des paramètres par défaut du volume.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="4e1cd-119">Si l’utilisateur existe déjà, aucune nouvelle entrée n’est créée.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="4e1cd-120">La méthode retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) associé à l’entrée existante.</span><span class="sxs-lookup"><span data-stu-id="4e1cd-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1cd-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4e1cd-121">Requirements</span></span>



| <span data-ttu-id="4e1cd-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e1cd-122">Requirement</span></span> | <span data-ttu-id="4e1cd-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e1cd-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1cd-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1cd-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e1cd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e1cd-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1cd-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e1cd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e1cd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1cd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e1cd-129"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4e1cd-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1cd-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e1cd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1cd-131">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4e1cd-132">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="4e1cd-133">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="4e1cd-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




