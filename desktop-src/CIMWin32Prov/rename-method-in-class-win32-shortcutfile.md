---
description: Renomme le fichier de raccourci (ou le répertoire) spécifié dans le chemin d’accès de l’objet.
ms.assetid: 6325fe96-19ee-4ccc-934c-ef0c0668f353
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c095a702269084a938887ef9717253df4653aea0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513119"
---
# <a name="rename-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="6fe0f-103">Renommer la méthode de la \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="6fe0f-103">Rename method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="6fe0f-104">La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le fichier de raccourci (ou le répertoire) spécifié dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="6fe0f-105">Un changement de nom n’est pas pris en charge si la destination se trouve sur un autre lecteur ou si le remplacement d’un fichier logique existant est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="6fe0f-106">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6fe0f-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6fe0f-107">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6fe0f-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe0f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe0f-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="6fe0f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe0f-110">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe0f-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-111">Nouveau nom complet du fichier (ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="6fe0f-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="6fe0f-112">Exemple : c : \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="6fe0f-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe0f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fe0f-113">Return value</span></span>

<span data-ttu-id="6fe0f-114">Retourne la valeur 0 (zéro) si le fichier a été renommé avec succès, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6fe0f-115">**0**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-116">La demande a abouti.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-117">**2**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-118">L’accès a été refusé.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-119">**8**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-120">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-121">**9**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-122">Le nom spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-123">**10**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-124">L’objet spécifié existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-125">**11**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-126">Le système de fichiers n’est pas NTFS.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-127">**12**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-128">La plateforme n’est pas Windows.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-129">**13**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-130">Le lecteur n’est pas le même.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-131">**14**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-132">Le répertoire n'est pas vide.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-133">**15**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-134">Une violation de partage s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-135">**16**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-136">Le fichier de démarrage spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-137">**17**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-138">Un privilège requis pour l’opération n’est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0f-139">**21**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6fe0f-140">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6fe0f-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fe0f-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe0f-141">Requirements</span></span>



| <span data-ttu-id="6fe0f-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fe0f-142">Requirement</span></span> | <span data-ttu-id="6fe0f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fe0f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe0f-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe0f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe0f-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fe0f-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fe0f-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe0f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe0f-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fe0f-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fe0f-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6fe0f-148">Namespace</span></span><br/>                | <span data-ttu-id="6fe0f-149">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6fe0f-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6fe0f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="6fe0f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fe0f-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fe0f-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fe0f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6fe0f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fe0f-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fe0f-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe0f-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe0f-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fe0f-155">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fe0f-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6fe0f-156">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="6fe0f-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

