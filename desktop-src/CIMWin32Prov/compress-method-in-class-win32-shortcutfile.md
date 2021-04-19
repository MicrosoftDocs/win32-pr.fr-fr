---
description: Compresse le fichier de raccourci logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: ade588a5-4e0c-486b-b187-805fcabbf326
ms.tgt_platform: multiple
title: Méthode Compress de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490f4d1a76844dc9ebad0449432f06833580d949
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516766"
---
# <a name="compress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="3e18c-103">Méthode Compress de la \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="3e18c-103">Compress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="3e18c-104">La méthode de classe **compresser** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) compresse le fichier de raccourci logique (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3e18c-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="3e18c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="3e18c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3e18c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3e18c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e18c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e18c-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="3e18c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e18c-108">Parameters</span></span>

<span data-ttu-id="3e18c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3e18c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e18c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e18c-110">Return value</span></span>

<span data-ttu-id="3e18c-111">Retourne la valeur 0 (zéro) si le fichier a été compressé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="3e18c-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3e18c-112">**0**</span><span class="sxs-lookup"><span data-stu-id="3e18c-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-113">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="3e18c-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-114">**2**</span><span class="sxs-lookup"><span data-stu-id="3e18c-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-115">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="3e18c-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-116">**8**</span><span class="sxs-lookup"><span data-stu-id="3e18c-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3e18c-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-118">**9**</span><span class="sxs-lookup"><span data-stu-id="3e18c-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-119">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3e18c-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-120">**10**</span><span class="sxs-lookup"><span data-stu-id="3e18c-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-121">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3e18c-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-122">**11**</span><span class="sxs-lookup"><span data-stu-id="3e18c-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-123">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="3e18c-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-124">**12**</span><span class="sxs-lookup"><span data-stu-id="3e18c-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-125">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="3e18c-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-126">**13**</span><span class="sxs-lookup"><span data-stu-id="3e18c-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-127">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="3e18c-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-128">**14**</span><span class="sxs-lookup"><span data-stu-id="3e18c-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-129">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="3e18c-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-130">**15**</span><span class="sxs-lookup"><span data-stu-id="3e18c-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-131">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3e18c-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-132">**16**</span><span class="sxs-lookup"><span data-stu-id="3e18c-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-133">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3e18c-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-134">**17**</span><span class="sxs-lookup"><span data-stu-id="3e18c-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-135">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="3e18c-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3e18c-136">**21**</span><span class="sxs-lookup"><span data-stu-id="3e18c-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3e18c-137">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3e18c-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e18c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e18c-138">Requirements</span></span>



| <span data-ttu-id="3e18c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e18c-139">Requirement</span></span> | <span data-ttu-id="3e18c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e18c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e18c-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e18c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3e18c-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e18c-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e18c-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e18c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3e18c-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e18c-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e18c-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3e18c-145">Namespace</span></span><br/>                | <span data-ttu-id="3e18c-146">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3e18c-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e18c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3e18c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e18c-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e18c-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e18c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3e18c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e18c-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e18c-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e18c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e18c-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e18c-152">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e18c-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3e18c-153">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="3e18c-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

