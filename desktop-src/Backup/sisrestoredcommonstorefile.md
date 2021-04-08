---
title: SisRestoredCommonStoreFile, fonction (sisbkup. h)
description: Signale à l’architecture SIS qu’un fichier de magasin commun a été écrit.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Sauvegarde de la fonction SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941856"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="1b733-104">SisRestoredCommonStoreFile fonction)</span><span class="sxs-lookup"><span data-stu-id="1b733-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="1b733-105">La fonction **SisRestoredCommonStoreFile** signale à l’architecture SIS qu’un fichier de magasin commun a été écrit.</span><span class="sxs-lookup"><span data-stu-id="1b733-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b733-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b733-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="1b733-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b733-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b733-108">*sisRestoreStructure* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b733-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b733-109">Pointeur vers une structure de restauration SIS retournée à partir de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="1b733-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b733-110">*commonStoreFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1b733-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b733-111">Nom du fichier de stockage commun restauré.</span><span class="sxs-lookup"><span data-stu-id="1b733-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b733-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b733-112">Return value</span></span>

<span data-ttu-id="1b733-113">Cette fonction retourne la **valeur true** si elle se termine avec succès et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1b733-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="1b733-114">Appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour obtenir plus d’informations sur la raison de l’échec de l’appel.</span><span class="sxs-lookup"><span data-stu-id="1b733-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b733-115">Notes</span><span class="sxs-lookup"><span data-stu-id="1b733-115">Remarks</span></span>

<span data-ttu-id="1b733-116">Cette fonction doit être appelée une fois que vous avez restauré un fichier de magasin commun.</span><span class="sxs-lookup"><span data-stu-id="1b733-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="1b733-117">Il informe l’architecture SIS qu’un nouveau fichier de magasin commun a été écrit, afin que l’architecture SIS puisse effectuer des tâches de maintenance internes, telles que l’initialisation de ses structures de données internes ou la résolution des liens vers le fichier de magasin commun.</span><span class="sxs-lookup"><span data-stu-id="1b733-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="1b733-118">Votre opération de restauration doit restaurer uniquement les fichiers du magasin commun signalés par [**SisRestoredLink**](sisrestoredlink.md), même s’il existe des fichiers de stockage commun supplémentaires sur le support de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="1b733-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="1b733-119">Votre opération de restauration peut restaurer les liens SIS et les fichiers du magasin commun dans l’ordre de leur choix. Toutefois, il doit appeler **SisRestoredLink** après la restauration d’un lien, et il doit appeler cette fonction après la restauration d’un fichier de magasin commun.</span><span class="sxs-lookup"><span data-stu-id="1b733-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="1b733-120">Étant donné que l’opération de restauration ne peut pas identifier les fichiers de magasin commun qui seront restaurés tant que les noms de fichiers ne sont pas signalés par la restauration d’un lien, votre opération de restauration restaurera toujours un fichier de magasin commun après qu’au moins un lien faisant référence à lui soit restauré.</span><span class="sxs-lookup"><span data-stu-id="1b733-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="1b733-121">Toutefois, vous pouvez ensuite restaurer des liens SIS supplémentaires qui pointent vers ce fichier de magasin commun.</span><span class="sxs-lookup"><span data-stu-id="1b733-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b733-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b733-122">Requirements</span></span>



| <span data-ttu-id="1b733-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b733-123">Requirement</span></span> | <span data-ttu-id="1b733-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b733-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b733-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b733-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1b733-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b733-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1b733-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b733-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1b733-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b733-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b733-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b733-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b733-130"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b733-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b733-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b733-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b733-132"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b733-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b733-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1b733-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b733-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b733-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b733-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b733-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b733-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="1b733-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="1b733-137">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="1b733-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

