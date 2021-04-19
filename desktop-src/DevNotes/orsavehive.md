---
description: Écrit la ruche de Registre hors connexion spécifiée dans un fichier.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: ORSaveHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539567"
---
# <a name="orsavehive-function"></a><span data-ttu-id="5e42d-103">ORSaveHive fonction)</span><span class="sxs-lookup"><span data-stu-id="5e42d-103">ORSaveHive function</span></span>

<span data-ttu-id="5e42d-104">Écrit la ruche de Registre hors connexion spécifiée dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5e42d-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e42d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e42d-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="5e42d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e42d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e42d-107">*Gérer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e42d-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e42d-108">Handle de la ruche de Registre hors connexion à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="5e42d-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="5e42d-109">*lpHivePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e42d-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e42d-110">Pointeur vers une chaîne Unicode qui spécifie le nom du fichier ruche du Registre.</span><span class="sxs-lookup"><span data-stu-id="5e42d-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="5e42d-111">Il ne peut pas s’agir du nom d’un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="5e42d-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="5e42d-112">*dwOsMajorVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e42d-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e42d-113">Numéro de version principale du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5e42d-113">The major version number of the operating system.</span></span> <span data-ttu-id="5e42d-114">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e42d-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="5e42d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e42d-115">Value</span></span>                                                                        | <span data-ttu-id="5e42d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="5e42d-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e42d-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="5e42d-118">Si *dwOsMinorVersion* est 1, le système d’exploitation est Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e42d-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="5e42d-119">Si *dwOsMinorVersion* est 2, le système d’exploitation est windows Server 2003 R2, windows Server 2003 ou Windows XP Professionnel Édition x64.</span><span class="sxs-lookup"><span data-stu-id="5e42d-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="5e42d-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="5e42d-121">Si *dwOsMinorVersion* est égal à 0, le système d’exploitation est windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e42d-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="5e42d-122">Si *dwOsMinorVersion* est 1, le système d’exploitation est windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e42d-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="5e42d-123">*dwOsMinorVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e42d-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e42d-124">Numéro de la version mineure du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5e42d-124">The minor version number of the operating system.</span></span> <span data-ttu-id="5e42d-125">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e42d-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="5e42d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e42d-126">Value</span></span>                                                                        | <span data-ttu-id="5e42d-127">Signification</span><span class="sxs-lookup"><span data-stu-id="5e42d-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e42d-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5e42d-129">Si *dwOsMajorVersion* est 6, le système d’exploitation est windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5e42d-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="5e42d-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5e42d-131">Si *dwOsMajorVersion* est 5, le système d’exploitation est Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e42d-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="5e42d-132">Si *dwOsMajorVersion* est 6, le système d’exploitation est windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5e42d-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5e42d-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5e42d-134">Si *dwOsMajorVersion* est 5, le système d’exploitation est windows Server 2003 R2, windows Server 2003 ou Windows XP Professionnel Édition x64.</span><span class="sxs-lookup"><span data-stu-id="5e42d-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="5e42d-135">Si *dwOsMajorVersion* a la valeur 6, le paramètre *dwOsMinorVersion* doit avoir la valeur 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="5e42d-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e42d-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e42d-136">Return value</span></span>

<span data-ttu-id="5e42d-137">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="5e42d-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5e42d-138">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="5e42d-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="5e42d-139">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="5e42d-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="5e42d-140">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5e42d-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="5e42d-141">Si l’appelant ne dispose pas des droits d’accès nécessaires pour écrire le fichier, la fonction retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="5e42d-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="5e42d-142">Si le fichier spécifié existe déjà, la fonction retourne l’erreur \_ déjà \_ existante.</span><span class="sxs-lookup"><span data-stu-id="5e42d-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e42d-143">Notes</span><span class="sxs-lookup"><span data-stu-id="5e42d-143">Remarks</span></span>

<span data-ttu-id="5e42d-144">La fonction **ORSaveHive** doit être utilisée pour enregistrer les modifications apportées à une ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5e42d-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="5e42d-145">Les modifications ne sont pas conservées tant que **ORSaveHive** n’est pas appelé pour enregistrer la ruche dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="5e42d-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="5e42d-146">Les paramètres *dwOsMajorVersion* et *dwOsMinorVersion* spécifient ensemble le format cible du fichier ruche du Registre.</span><span class="sxs-lookup"><span data-stu-id="5e42d-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="5e42d-147">Le tableau suivant récapitule les numéros de version des systèmes d’exploitation les plus récents.</span><span class="sxs-lookup"><span data-stu-id="5e42d-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="5e42d-148">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="5e42d-148">Operating system</span></span>                    | <span data-ttu-id="5e42d-149">Numéro de version</span><span class="sxs-lookup"><span data-stu-id="5e42d-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="5e42d-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e42d-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="5e42d-151">6.1</span><span class="sxs-lookup"><span data-stu-id="5e42d-151">6.1</span></span>            |
| <span data-ttu-id="5e42d-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e42d-152">Windows 7</span></span>                           | <span data-ttu-id="5e42d-153">6.1</span><span class="sxs-lookup"><span data-stu-id="5e42d-153">6.1</span></span>            |
| <span data-ttu-id="5e42d-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e42d-154">Windows Server 2008</span></span>                 | <span data-ttu-id="5e42d-155">6.0</span><span class="sxs-lookup"><span data-stu-id="5e42d-155">6.0</span></span>            |
| <span data-ttu-id="5e42d-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e42d-156">Windows Vista</span></span>                       | <span data-ttu-id="5e42d-157">6.0</span><span class="sxs-lookup"><span data-stu-id="5e42d-157">6.0</span></span>            |
| <span data-ttu-id="5e42d-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5e42d-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="5e42d-159">5.2</span><span class="sxs-lookup"><span data-stu-id="5e42d-159">5.2</span></span>            |
| <span data-ttu-id="5e42d-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5e42d-160">Windows Server 2003</span></span>                 | <span data-ttu-id="5e42d-161">5.2</span><span class="sxs-lookup"><span data-stu-id="5e42d-161">5.2</span></span>            |
| <span data-ttu-id="5e42d-162">Windows XP Professionnel Édition x64</span><span class="sxs-lookup"><span data-stu-id="5e42d-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="5e42d-163">5.2</span><span class="sxs-lookup"><span data-stu-id="5e42d-163">5.2</span></span>            |
| <span data-ttu-id="5e42d-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5e42d-164">Windows XP</span></span>                          | <span data-ttu-id="5e42d-165">5,1</span><span class="sxs-lookup"><span data-stu-id="5e42d-165">5.1</span></span>            |



 

<span data-ttu-id="5e42d-166">Utilisez la fonction [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) pour récupérer des informations sur le système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="5e42d-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="5e42d-167">La fonction **ORSaveHive** verrouille la ruche du Registre pendant qu’elle écrit la ruche dans le fichier, puis ferme le fichier et libère le verrou.</span><span class="sxs-lookup"><span data-stu-id="5e42d-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="5e42d-168">La ruche du Registre reste en mémoire jusqu’à ce qu’elle soit fermée par l’appel de la fonction [**ORCloseHive**](orclosehive.md) .</span><span class="sxs-lookup"><span data-stu-id="5e42d-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="5e42d-169">Il est possible d’apporter d’autres modifications à la ruche du Registre pendant qu’elle est ouverte ; Toutefois, pour conserver ces modifications, la ruche doit être enregistrée dans un nouveau fichier, car la fonction **ORSaveHive** ne remplacera pas un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="5e42d-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="5e42d-170">La fonction **ORSaveHive** peut être utilisée pour enregistrer une partie de la ruche de Registre hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5e42d-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="5e42d-171">La clé spécifiée dans le paramètre *handle* devient la clé racine d’une ruche qui se compose de la clé spécifiée et de toutes ses sous-clés.</span><span class="sxs-lookup"><span data-stu-id="5e42d-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e42d-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e42d-172">Requirements</span></span>



| <span data-ttu-id="5e42d-173">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e42d-173">Requirement</span></span> | <span data-ttu-id="5e42d-174">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e42d-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e42d-175">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5e42d-175">Redistributable</span></span><br/> | <span data-ttu-id="5e42d-176">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="5e42d-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="5e42d-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e42d-177">Header</span></span><br/>          | <dl> <span data-ttu-id="5e42d-178"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e42d-179">DLL</span><span class="sxs-lookup"><span data-stu-id="5e42d-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="5e42d-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e42d-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e42d-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e42d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e42d-182">Tourne</span><span class="sxs-lookup"><span data-stu-id="5e42d-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="5e42d-183">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="5e42d-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="5e42d-184">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="5e42d-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
