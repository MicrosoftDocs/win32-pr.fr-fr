---
description: Retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Méthode GetAccessMask de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950560"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="175bc-103">Méthode GetAccessMask de la \_ classe de partage Win32</span><span class="sxs-lookup"><span data-stu-id="175bc-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="175bc-104">La méthode **GetAccessMask** retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.</span><span class="sxs-lookup"><span data-stu-id="175bc-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="175bc-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="175bc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="175bc-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="175bc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="175bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="175bc-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="175bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="175bc-108">Parameters</span></span>

<span data-ttu-id="175bc-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="175bc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="175bc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="175bc-110">Return value</span></span>

<span data-ttu-id="175bc-111">Droits d’accès au partage détenu par l’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="175bc-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="175bc-112">**\_Répertoire de liste de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="175bc-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="175bc-113">1 (0x1)</span></span>

<span data-ttu-id="175bc-114">Accorde le droit de lire des données à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="175bc-115">Pour un répertoire, cette valeur accorde le droit de répertorier le contenu du répertoire.</span><span class="sxs-lookup"><span data-stu-id="175bc-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-116">**fichier \_ ajouter \_ un fichier**</span><span class="sxs-lookup"><span data-stu-id="175bc-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-117">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="175bc-117">2 (0x2)</span></span>

<span data-ttu-id="175bc-118">Accorde le droit d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="175bc-119">Pour un répertoire, cette valeur accorde le droit de créer un fichier dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="175bc-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-120">**FICHIER \_ Ajouter un \_ sous-répertoire**</span><span class="sxs-lookup"><span data-stu-id="175bc-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="175bc-121">4 (0x4)</span></span>

<span data-ttu-id="175bc-122">Accorde le droit d’ajouter des données au fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="175bc-123">Pour un répertoire, cette valeur accorde le droit de créer un sous-répertoire.</span><span class="sxs-lookup"><span data-stu-id="175bc-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-124">**lecture de fichier \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="175bc-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="175bc-125">8 (0x8)</span></span>

<span data-ttu-id="175bc-126">Accorde le droit de lire les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="175bc-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-127">**écriture de fichier \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="175bc-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="175bc-128">16 (0x10)</span></span>

<span data-ttu-id="175bc-129">Accorde le droit d’écrire des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="175bc-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-130">**parcours de fichiers \_**</span><span class="sxs-lookup"><span data-stu-id="175bc-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="175bc-131">32 (0x20)</span></span>

<span data-ttu-id="175bc-132">Accorde le droit d’exécuter un fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-132">Grants the right to execute a file.</span></span> <span data-ttu-id="175bc-133">Pour un répertoire, le répertoire peut être parcouru.</span><span class="sxs-lookup"><span data-stu-id="175bc-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-134">**\_supprimer un \_ enfant de fichier**</span><span class="sxs-lookup"><span data-stu-id="175bc-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="175bc-135">64 (0x40)</span></span>

<span data-ttu-id="175bc-136">Accorde le droit de supprimer un répertoire et tous les fichiers qu’il contient (ses enfants), même si les fichiers sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="175bc-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-137">**\_attributs de lecture de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="175bc-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="175bc-138">128 (0x80)</span></span>

<span data-ttu-id="175bc-139">Accorde le droit de lire les attributs du fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-140">**\_attributs d’écriture de fichier \_**</span><span class="sxs-lookup"><span data-stu-id="175bc-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="175bc-141">256 (0x100)</span></span>

<span data-ttu-id="175bc-142">Accorde le droit de modifier les attributs de fichier.</span><span class="sxs-lookup"><span data-stu-id="175bc-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="175bc-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="175bc-144">65536 (0x10000)</span></span>

<span data-ttu-id="175bc-145">Octroie l’accès en suppression.</span><span class="sxs-lookup"><span data-stu-id="175bc-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-146">**LIRE \_ le contrôle**</span><span class="sxs-lookup"><span data-stu-id="175bc-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="175bc-147">131072 (0x20000)</span></span>

<span data-ttu-id="175bc-148">Octroie l’accès en lecture au descripteur de sécurité et au propriétaire.</span><span class="sxs-lookup"><span data-stu-id="175bc-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-149">**ÉCRITURE \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="175bc-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="175bc-150">262144 (0x40000)</span></span>

<span data-ttu-id="175bc-151">Accorde un accès en écriture à la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="175bc-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="175bc-152">**propriétaire en écriture \_**</span><span class="sxs-lookup"><span data-stu-id="175bc-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="175bc-153">524288 (0x80000)</span></span>

<span data-ttu-id="175bc-154">Affecte le propriétaire de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="175bc-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="175bc-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="175bc-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="175bc-156">1048576 ()</span><span class="sxs-lookup"><span data-stu-id="175bc-156">1048576 (0x100000)</span></span>

<span data-ttu-id="175bc-157">Synchronise l’accès et permet à un processus d’attendre qu’un objet passe à l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="175bc-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="175bc-158">Notes</span><span class="sxs-lookup"><span data-stu-id="175bc-158">Remarks</span></span>

<span data-ttu-id="175bc-159">La méthode **GetAccessMask** est une méthode d’objet qui est utilisée sur une occurrence de cette classe.</span><span class="sxs-lookup"><span data-stu-id="175bc-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="175bc-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="175bc-160">Examples</span></span>

<span data-ttu-id="175bc-161">L’exemple de code VBScript suivant crée un dossier de partage, puis obtient la valeur du masque d’accès dans le descripteur de sécurité qui sécurise le dossier de partage.</span><span class="sxs-lookup"><span data-stu-id="175bc-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="175bc-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="175bc-162">Requirements</span></span>



| <span data-ttu-id="175bc-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="175bc-163">Requirement</span></span> | <span data-ttu-id="175bc-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="175bc-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="175bc-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175bc-165">Minimum supported client</span></span><br/> | <span data-ttu-id="175bc-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="175bc-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="175bc-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="175bc-167">Minimum supported server</span></span><br/> | <span data-ttu-id="175bc-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="175bc-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="175bc-169">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="175bc-169">Namespace</span></span><br/>                | <span data-ttu-id="175bc-170">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="175bc-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="175bc-171">MOF</span><span class="sxs-lookup"><span data-stu-id="175bc-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="175bc-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="175bc-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="175bc-173">DLL</span><span class="sxs-lookup"><span data-stu-id="175bc-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="175bc-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="175bc-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175bc-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="175bc-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175bc-176">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="175bc-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

