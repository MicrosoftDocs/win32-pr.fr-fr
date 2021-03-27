---
description: Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.
title: Méthode DiskQuotaControl. FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971966"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="7d810-103">Méthode DiskQuotaControl. FindUser</span><span class="sxs-lookup"><span data-stu-id="7d810-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="7d810-104">Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.</span><span class="sxs-lookup"><span data-stu-id="7d810-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d810-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d810-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="7d810-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d810-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d810-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="7d810-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="7d810-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7d810-108">Type: **String**</span></span>

<span data-ttu-id="7d810-109">Valeur de chaîne qui contient le nom d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7d810-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d810-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d810-110">Return value</span></span>

<span data-ttu-id="7d810-111">Retourne une expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7d810-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d810-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7d810-112">Remarks</span></span>

<span data-ttu-id="7d810-113">Cette méthode retourne un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) même s’il n’y a aucune entrée pour l’utilisateur dans le fichier de quota.</span><span class="sxs-lookup"><span data-stu-id="7d810-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="7d810-114">Le seuil d’avertissement et les limites de quota matériel sont définis pour l’objet utilisateur retourné sur les valeurs par défaut du volume.</span><span class="sxs-lookup"><span data-stu-id="7d810-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="7d810-115">La chaîne retournée par [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) peut être passée à la place du paramètre *sLogonName* .</span><span class="sxs-lookup"><span data-stu-id="7d810-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="7d810-116">Quand **FindUser** reçoit une chaîne sid, il utilise le SID correspondant pour la recherche directe de l’enregistrement de quota de l’utilisateur sur le volume.</span><span class="sxs-lookup"><span data-stu-id="7d810-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="7d810-117">Cela contourne le cache de noms SID.</span><span class="sxs-lookup"><span data-stu-id="7d810-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="7d810-118">Dans les cas où **FindUser** échoue en raison d’une incompatibilité de format (par exemple, compatible Sam et UPN) du nom d’ouverture de session fourni et du nom d’ouverture de session mis en cache, le nom d’ouverture de session peut être traduit en une chaîne sid à l’aide de **TranslateLogonNameToSID** , puis retransmis à **FindUser**.</span><span class="sxs-lookup"><span data-stu-id="7d810-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="7d810-119">Le code VBScript suivant illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="7d810-119">The following VBScript code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a><span data-ttu-id="7d810-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d810-120">Requirements</span></span>



| <span data-ttu-id="7d810-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d810-121">Requirement</span></span> | <span data-ttu-id="7d810-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d810-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d810-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d810-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7d810-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d810-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d810-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d810-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7d810-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d810-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7d810-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7d810-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d810-128"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="7d810-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d810-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d810-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d810-130">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="7d810-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




