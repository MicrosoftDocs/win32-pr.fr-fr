---
description: La méthode FileHash de l’objet installer prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier. Les informations de hachage de fichier sont retournées en tant qu’objet enregistrement. L’intégralité du hachage de fichier 128 bits est retournée en tant que champs de propriété IntegerData 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer. FileHash, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528777"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="3399c-105">Installer. FileHash, méthode</span><span class="sxs-lookup"><span data-stu-id="3399c-105">Installer.FileHash method</span></span>

<span data-ttu-id="3399c-106">La méthode **FileHash** de l' [**objet installer**](installer-object.md) prend le chemin d’accès à un fichier et retourne un hachage 128 bits de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3399c-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="3399c-107">Les informations de hachage de fichier sont retournées en tant qu' [**objet enregistrement**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="3399c-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="3399c-108">L’intégralité du hachage de fichier 128 bits est retournée en tant que champs de propriété [**IntegerData**](record-integerdata.md) 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3399c-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="3399c-109">Les valeurs retournées dans l' [**objet record**](record-object.md) correspondent aux quatre champs de la structure [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) retournée par [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="3399c-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="3399c-110">La numérotation de quatre champs est basée sur 1 dans la [table MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="3399c-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="3399c-111">Le champ 1 correspond à la colonne HashPart1.</span><span class="sxs-lookup"><span data-stu-id="3399c-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="3399c-112">Le champ 2 correspond à la colonne HashPart2.</span><span class="sxs-lookup"><span data-stu-id="3399c-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="3399c-113">Le champ 3 correspond à la colonne HashPart3.</span><span class="sxs-lookup"><span data-stu-id="3399c-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="3399c-114">Le champ 4 correspond à la colonne HashPart4.</span><span class="sxs-lookup"><span data-stu-id="3399c-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="3399c-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3399c-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="3399c-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3399c-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3399c-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="3399c-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="3399c-118">Chemin d’accès au fichier à hacher.</span><span class="sxs-lookup"><span data-stu-id="3399c-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="3399c-119">*Options*</span><span class="sxs-lookup"><span data-stu-id="3399c-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="3399c-120">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="3399c-120">Reserved for future use.</span></span>

<span data-ttu-id="3399c-121">La valeur de ce paramètre doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="3399c-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3399c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3399c-122">Return value</span></span>

<span data-ttu-id="3399c-123">En cas de réussite, cette méthode retourne un [**objet enregistrement**](record-object.md) qui contient le hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="3399c-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3399c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3399c-124">Requirements</span></span>



| <span data-ttu-id="3399c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3399c-125">Requirement</span></span> | <span data-ttu-id="3399c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3399c-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3399c-127">Version</span><span class="sxs-lookup"><span data-stu-id="3399c-127">Version</span></span><br/> | <span data-ttu-id="3399c-128">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3399c-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3399c-129">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3399c-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3399c-130">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="3399c-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3399c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3399c-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="3399c-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3399c-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3399c-133">IID</span><span class="sxs-lookup"><span data-stu-id="3399c-133">IID</span></span><br/>     | <span data-ttu-id="3399c-134">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3399c-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3399c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3399c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3399c-136">Contrôle de version de fichier par défaut</span><span class="sxs-lookup"><span data-stu-id="3399c-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="3399c-137">Gérer les tailles et les versions des fichiers</span><span class="sxs-lookup"><span data-stu-id="3399c-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="3399c-138">Table MsiFileHash</span><span class="sxs-lookup"><span data-stu-id="3399c-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="3399c-139">**MsiGetFileHash**</span><span class="sxs-lookup"><span data-stu-id="3399c-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




