---
description: Crée la clé de Registre spécifiée dans une ruche de Registre hors connexion. Si la clé existe déjà, la fonction l’ouvre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: ORCreateKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528972"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="98bca-104">ORCreateKey fonction)</span><span class="sxs-lookup"><span data-stu-id="98bca-104">ORCreateKey function</span></span>

<span data-ttu-id="98bca-105">Crée la clé de Registre spécifiée dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="98bca-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="98bca-106">Si la clé existe déjà, la fonction l’ouvre.</span><span class="sxs-lookup"><span data-stu-id="98bca-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98bca-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="98bca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98bca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98bca-109">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98bca-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-110">Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="98bca-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="98bca-111">*lpSubKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98bca-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-112">Pointeur vers une chaîne Unicode qui contient le nom d’une sous-clé que cette fonction ouvre ou crée.</span><span class="sxs-lookup"><span data-stu-id="98bca-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="98bca-113">Le paramètre *lpSubKey* doit spécifier une sous-clé de la clé identifiée par le paramètre *handle* ; Il peut atteindre jusqu’à 32 niveaux de profondeur dans l’arborescence du Registre.</span><span class="sxs-lookup"><span data-stu-id="98bca-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="98bca-114">Pour plus d’informations sur les noms de clé, consultez [structure du Registre](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="98bca-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="98bca-115">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="98bca-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="98bca-116">Les noms de clés ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="98bca-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="98bca-117">*lpClass* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="98bca-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-118">Classe (type d’objet) de cette clé.</span><span class="sxs-lookup"><span data-stu-id="98bca-118">The class (object type) of this key.</span></span> <span data-ttu-id="98bca-119">Ce paramètre peut être ignoré.</span><span class="sxs-lookup"><span data-stu-id="98bca-119">This parameter may be ignored.</span></span> <span data-ttu-id="98bca-120">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="98bca-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="98bca-121">*dwOptions* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="98bca-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-122">Ce paramètre peut avoir la valeur 0 ou l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="98bca-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="98bca-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="98bca-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="98bca-124">Signification</span><span class="sxs-lookup"><span data-stu-id="98bca-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="98bca-125"><dt>**Reg \_ OPTION de \_ création de \_ lien**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="98bca-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="98bca-126">La clé est un lien symbolique.</span><span class="sxs-lookup"><span data-stu-id="98bca-126">The key is a symbolic link.</span></span> <span data-ttu-id="98bca-127">Le chemin d’accès cible est assigné à la valeur de L' « SymbolicLinkValue » de la clé.</span><span class="sxs-lookup"><span data-stu-id="98bca-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="98bca-128">Le chemin d’accès cible doit être un chemin d’accès absolu au registre.</span><span class="sxs-lookup"><span data-stu-id="98bca-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="98bca-129">Si cette option est définie, **l' \_ option reg \_ non \_ volatile** doit également être définie.</span><span class="sxs-lookup"><span data-stu-id="98bca-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="98bca-130">Si le paramètre *lpSubKey* spécifie une clé existante, il doit avoir été créé avec l' **\_ option reg \_ Create \_ Link**.</span><span class="sxs-lookup"><span data-stu-id="98bca-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="98bca-131">Les liens symboliques du Registre doivent être utilisés uniquement lorsque cela est absolument nécessaire pour la compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="98bca-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="98bca-132"><dt>**Reg \_ OPTION \_ non \_ volatile**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="98bca-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="98bca-133">La clé n’est pas volatile. Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="98bca-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="98bca-134">Les informations sont stockées dans un fichier et sont conservées lorsque le système est redémarré.</span><span class="sxs-lookup"><span data-stu-id="98bca-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="98bca-135">La fonction [**ORSaveHive**](orsavehive.md) enregistre les clés qui ne sont pas volatiles.</span><span class="sxs-lookup"><span data-stu-id="98bca-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="98bca-136">*pSecurityDescriptor* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="98bca-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-137">Pointeur vers une structure [de \_ descripteur de sécurité](/windows/win32/api/winnt/ns-winnt-security_descriptor) qui contient un descripteur de sécurité pour la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="98bca-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="98bca-138">Si *pSecurityDescriptor* a la **valeur null**, la clé obtient un descripteur de sécurité par défaut.</span><span class="sxs-lookup"><span data-stu-id="98bca-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="98bca-139">Les listes de contrôle d’accès dans un descripteur de sécurité par défaut pour une clé sont héritées de sa clé parente directe.</span><span class="sxs-lookup"><span data-stu-id="98bca-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="98bca-140">*phkResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="98bca-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-141">Pointeur vers une variable qui reçoit un handle vers la clé ouverte ou créée.</span><span class="sxs-lookup"><span data-stu-id="98bca-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="98bca-142">Utilisez la fonction [**ORCloseKey**](orclosekey.md) pour fermer la clé une fois que vous avez fini d’utiliser le handle.</span><span class="sxs-lookup"><span data-stu-id="98bca-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="98bca-143">*pdwDisposition* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="98bca-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98bca-144">Pointeur vers une variable qui reçoit l’une des valeurs de disposition suivantes.</span><span class="sxs-lookup"><span data-stu-id="98bca-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="98bca-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="98bca-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="98bca-146">Signification</span><span class="sxs-lookup"><span data-stu-id="98bca-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="98bca-147"><dt>**Reg \_ \_Nouvelle \_ clé**</dt> <dt>0x00000001L</dt> créée</span><span class="sxs-lookup"><span data-stu-id="98bca-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="98bca-148">La clé n’existait pas et a été créée.</span><span class="sxs-lookup"><span data-stu-id="98bca-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="98bca-149"><dt>**Reg \_ 0x00000002L \_ \_ clé existante ouverte**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="98bca-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="98bca-150">La clé existait et a simplement été ouverte sans être modifiée.</span><span class="sxs-lookup"><span data-stu-id="98bca-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="98bca-151">Si *pdwDisposition* a la **valeur null**, aucune information de disposition n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="98bca-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98bca-152">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98bca-152">Return value</span></span>

<span data-ttu-id="98bca-153">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="98bca-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="98bca-154">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="98bca-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="98bca-155">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="98bca-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="98bca-156">Si le paramètre *dwOptions* est défini avec **l' \_ option reg \_ Create \_ Link** mais que l' **\_ option reg \_ non \_ volatile** est désactivée, ou si le handle à retourner est un descripteur de la clé racine de Hive, la fonction retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="98bca-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="98bca-157">Notes</span><span class="sxs-lookup"><span data-stu-id="98bca-157">Remarks</span></span>

<span data-ttu-id="98bca-158">La clé créée par la fonction **ORCreateKey** n’a pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="98bca-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="98bca-159">Une application peut utiliser la fonction [**ORSetValue**](orsetvalue.md) pour définir des valeurs de clés.</span><span class="sxs-lookup"><span data-stu-id="98bca-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="98bca-160">La fonction **ORCreateKey** ne peut pas être utilisée pour créer la clé racine dans une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="98bca-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="98bca-161">Utilisez la fonction [**ORCreateHive**](orcreatehive.md) pour créer la clé racine et obtenir un descripteur de la clé.</span><span class="sxs-lookup"><span data-stu-id="98bca-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="98bca-162">Le registre hors connexion ne prend pas en charge l’enregistrement de clés individuelles.</span><span class="sxs-lookup"><span data-stu-id="98bca-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="98bca-163">Utilisez la fonction [**ORSaveHive**](orsavehive.md) pour enregistrer une clé et ses sous-clés dans une ruche.</span><span class="sxs-lookup"><span data-stu-id="98bca-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="98bca-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98bca-164">Requirements</span></span>



| <span data-ttu-id="98bca-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98bca-165">Requirement</span></span> | <span data-ttu-id="98bca-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="98bca-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98bca-167">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="98bca-167">Redistributable</span></span><br/> | <span data-ttu-id="98bca-168">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="98bca-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="98bca-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="98bca-169">Header</span></span><br/>          | <dl> <span data-ttu-id="98bca-170"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="98bca-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="98bca-171">DLL</span><span class="sxs-lookup"><span data-stu-id="98bca-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="98bca-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98bca-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98bca-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98bca-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bca-174">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="98bca-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="98bca-175">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="98bca-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="98bca-176">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="98bca-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="98bca-177">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="98bca-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="98bca-178">descripteur de sécurité \_</span><span class="sxs-lookup"><span data-stu-id="98bca-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
