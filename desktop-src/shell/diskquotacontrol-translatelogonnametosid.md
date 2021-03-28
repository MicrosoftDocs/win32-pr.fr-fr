---
description: Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.
title: Méthode DiskQuotaControl. TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034823"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="75cad-103">Méthode DiskQuotaControl. TranslateLogonNameToSID</span><span class="sxs-lookup"><span data-stu-id="75cad-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="75cad-104">Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="75cad-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="75cad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75cad-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="75cad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75cad-107">*logonname*</span><span class="sxs-lookup"><span data-stu-id="75cad-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="75cad-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="75cad-108">Type: **String**</span></span>

<span data-ttu-id="75cad-109">Valeur de chaîne qui spécifie le nom d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75cad-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75cad-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75cad-110">Return value</span></span>

<span data-ttu-id="75cad-111">Retourne l’ID de sécurité (SID) de l’utilisateur au format chaîne correspondant au nom d’ouverture de session fourni.</span><span class="sxs-lookup"><span data-stu-id="75cad-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="75cad-112">La chaîne retournée comprend les accolades fermantes standard.</span><span class="sxs-lookup"><span data-stu-id="75cad-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="75cad-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="75cad-113">For example:</span></span>

<span data-ttu-id="75cad-114">« {S-1-5-21-2127521184-1604012920-1887927527-19009} »</span><span class="sxs-lookup"><span data-stu-id="75cad-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="75cad-115">Notes</span><span class="sxs-lookup"><span data-stu-id="75cad-115">Remarks</span></span>

<span data-ttu-id="75cad-116">La chaîne SID retournée peut être transmise à la méthode [**FindUser**](diskquotacontrol-finduser.md) à la place d’un nom d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="75cad-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="75cad-117">Lorsqu’un appel à la méthode [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) échoue, cela peut être dû à une incompatibilité entre le formulaire (par exemple, le gestionnaire de compte de sécurité \[ sam \] compatible et le nom d’utilisateur principal \[ UPN \] ) du nom d’ouverture de session fourni et le formulaire stocké dans le cache sid-Name.</span><span class="sxs-lookup"><span data-stu-id="75cad-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="75cad-118">Dans ce cas, le nom d’ouverture de session peut être converti en SID et l’appel à **FindUser** est répété.</span><span class="sxs-lookup"><span data-stu-id="75cad-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="75cad-119">**FindUser** reconnaît une chaîne sid et contourne la recherche de cache de nom sid.</span><span class="sxs-lookup"><span data-stu-id="75cad-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="75cad-120">Le code Microsoft Visual Basic Scripting Edition (VBScript) suivant illustre cette technique.</span><span class="sxs-lookup"><span data-stu-id="75cad-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


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



<span data-ttu-id="75cad-121">La traduction de nom à SID peut être un processus lent par rapport aux recherches dans le cache SID-Name.</span><span class="sxs-lookup"><span data-stu-id="75cad-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="75cad-122">Par conséquent, il est recommandé d’appeler d’abord [**FindUser**](diskquotacontrol-finduser.md) avec un nom d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="75cad-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="75cad-123">L’exemple ci-dessus utilise cette technique.</span><span class="sxs-lookup"><span data-stu-id="75cad-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="75cad-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="75cad-124">Requirements</span></span>



| <span data-ttu-id="75cad-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75cad-125">Requirement</span></span> | <span data-ttu-id="75cad-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="75cad-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75cad-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75cad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="75cad-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75cad-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75cad-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75cad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="75cad-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75cad-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="75cad-131">DLL</span><span class="sxs-lookup"><span data-stu-id="75cad-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75cad-132"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="75cad-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75cad-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75cad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75cad-134">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="75cad-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




