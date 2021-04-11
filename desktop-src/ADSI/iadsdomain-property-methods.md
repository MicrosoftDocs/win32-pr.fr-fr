---
title: Méthodes de propriété IADsDomain (IADs. h)
description: Les méthodes de l’interface IADsDomain lisent et écrivent les propriétés décrites dans cette rubrique. Pour plus d’informations, consultez Méthodes de propriété d’interface.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsDomain ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942572"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="45278-105">Méthodes de propriété IADsDomain</span><span class="sxs-lookup"><span data-stu-id="45278-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="45278-106">Les méthodes de l’interface [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) lisent et écrivent les propriétés décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="45278-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="45278-107">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="45278-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="45278-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45278-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="45278-109">**AutoUnlockInterval**</span><span class="sxs-lookup"><span data-stu-id="45278-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="45278-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-111">Indique la durée minimale qui doit s’écouler avant que le compte ne soit automatiquement réactivé.</span><span class="sxs-lookup"><span data-stu-id="45278-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="45278-112">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-114">**IsWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="45278-114">**IsWorkgroup**</span></span>
<span data-ttu-id="45278-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-116">Cette propriété n’est plus implémentée.</span><span class="sxs-lookup"><span data-stu-id="45278-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="45278-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45278-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45278-118">Type de données de script : **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="45278-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-119">**LockoutObservationInterval**</span><span class="sxs-lookup"><span data-stu-id="45278-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="45278-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-121">Indique la fenêtre de temps pendant laquelle le nombre de mots de passe incorrects est surveillé et accumulé avant de déterminer si le compte doit être verrouillé. Par exemple, si le nombre de tentatives de mot de passe incorrectes sur un compte dépasse le seuil (nombre maximal de mots de passe incorrects autorisé) au cours de la période spécifiée (intervalle d’observation du verrouillage), le compte est verrouillé en définissant la propriété appropriée dans le jeu de propriétés de paramètre de connexion.</span><span class="sxs-lookup"><span data-stu-id="45278-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="45278-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-123">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-124">**MaxBadPasswordsAllowed**</span><span class="sxs-lookup"><span data-stu-id="45278-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="45278-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-126">Indique le nombre maximal de connexions de mot de passe incorrectes autorisées avant le verrouillage d’un compte.</span><span class="sxs-lookup"><span data-stu-id="45278-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="45278-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-128">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-129">**MaxPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="45278-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="45278-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-131">Indique l’intervalle de temps maximal, en secondes, au terme duquel le mot de passe doit être modifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="45278-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="45278-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-133">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-134">**MinPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="45278-134">**MinPasswordAge**</span></span>
<span data-ttu-id="45278-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-136">Indique l’intervalle de temps minimal, en secondes, avant que le mot de passe ne puisse être modifié.</span><span class="sxs-lookup"><span data-stu-id="45278-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="45278-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-138">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-139">**MinPasswordLength**</span><span class="sxs-lookup"><span data-stu-id="45278-139">**MinPasswordLength**</span></span>
<span data-ttu-id="45278-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-141">Indique le nombre minimal de caractères qui doivent être utilisés pour un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="45278-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="45278-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-143">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-144">**PasswordAttributes**</span><span class="sxs-lookup"><span data-stu-id="45278-144">**PasswordAttributes**</span></span>
<span data-ttu-id="45278-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-146">Indique des restrictions sur les mots de passe, tels que définis dans la liste d’attributs et de valeurs suivante.</span><span class="sxs-lookup"><span data-stu-id="45278-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="45278-147">Pour \_ \_ la complexité du mot de passe, le mot de passe doit inclure au moins un signe de ponctuation ou un caractère non imprimable.</span><span class="sxs-lookup"><span data-stu-id="45278-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="45278-148">**Mot de passe \_ ATTR \_ None** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="45278-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="45278-149">**Mot de passe \_ \_ \_ Casse mixte attr** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="45278-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="45278-150">**Mot de passe \_ \_Complexe attr** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="45278-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="45278-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-152">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="45278-153">**PasswordHistoryLength**</span><span class="sxs-lookup"><span data-stu-id="45278-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="45278-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45278-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="45278-155">Indique le nombre de mots de passe précédents enregistrés dans la liste historique.</span><span class="sxs-lookup"><span data-stu-id="45278-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="45278-156">L’utilisateur ne peut pas réutiliser un mot de passe dans la liste historique.</span><span class="sxs-lookup"><span data-stu-id="45278-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="45278-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45278-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="45278-158">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="45278-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="45278-159">Exemples</span><span class="sxs-lookup"><span data-stu-id="45278-159">Examples</span></span>

<span data-ttu-id="45278-160">L’exemple de code suivant affiche la valeur de la propriété **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="45278-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="45278-161">L’exemple de code suivant affiche la valeur de la propriété **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="45278-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="45278-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45278-162">Requirements</span></span>



| <span data-ttu-id="45278-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45278-163">Requirement</span></span> | <span data-ttu-id="45278-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="45278-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45278-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45278-165">Minimum supported client</span></span><br/> | <span data-ttu-id="45278-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45278-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45278-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45278-167">Minimum supported server</span></span><br/> | <span data-ttu-id="45278-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45278-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45278-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="45278-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="45278-170"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="45278-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="45278-171">DLL</span><span class="sxs-lookup"><span data-stu-id="45278-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45278-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45278-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="45278-173">IID</span><span class="sxs-lookup"><span data-stu-id="45278-173">IID</span></span><br/>                      | <span data-ttu-id="45278-174">IID \_ IADsDomain est défini en tant que 00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="45278-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="45278-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45278-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45278-176">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="45278-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="45278-177">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="45278-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





