---
description: Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier. La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Méthode temps de la classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202215"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="63f44-104">Méthode temps de la \_ classe CollectionSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="63f44-104">ExportSnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="63f44-105">Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="63f44-105">Exports a snapshot collection of virtual computer systems to a file.</span></span> <span data-ttu-id="63f44-106">La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="63f44-106">The snapshot collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f44-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63f44-107">Syntax</span></span>


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="63f44-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63f44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f44-109">*SnapshotCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63f44-109">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f44-110">Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection d’instantanés à exporter.</span><span class="sxs-lookup"><span data-stu-id="63f44-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="63f44-111">*ExportDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63f44-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f44-112">Chemin d’accès complet du répertoire dans lequel la collection de systèmes virtuels doit être exportée.</span><span class="sxs-lookup"><span data-stu-id="63f44-112">The fully-qualified path of the directory to which the virtual system collection is to be exported.</span></span> <span data-ttu-id="63f44-113">Si la propriété **CreateVmExportSubdirectory** dans le paramètre *ExportSettingData* est définie sur **true** , ce répertoire peut être réutilisé pour l’exportation de plusieurs collections de systèmes virtuels et cette méthode place chaque définition de collection de système virtuel dans un sous-répertoire distinct sous ce chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="63f44-113">If the **CreateVmExportSubdirectory** property in the *ExportSettingData* parameter is set to **True** then this directory can be reused for exporting multiple virtual system collections and this method places each virtual system collection definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="63f44-114">*ExportSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63f44-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63f44-115">Instance de [**MSVM \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="63f44-115">An instance of [**Msvm\_CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="63f44-116">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="63f44-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63f44-117">Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="63f44-117">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="63f44-118">Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="63f44-118">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f44-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63f44-119">Return value</span></span>

<span data-ttu-id="63f44-120">Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit.</span><span class="sxs-lookup"><span data-stu-id="63f44-120">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="63f44-121">Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la tâche peut être utilisé pour suivre la progression de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="63f44-121">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="63f44-122">Toute autre valeur de retour indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="63f44-122">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="63f44-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63f44-123">Requirements</span></span>



| <span data-ttu-id="63f44-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63f44-124">Requirement</span></span> | <span data-ttu-id="63f44-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="63f44-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f44-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63f44-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63f44-127">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63f44-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="63f44-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63f44-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63f44-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="63f44-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="63f44-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63f44-130">Namespace</span></span><br/>                | <span data-ttu-id="63f44-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="63f44-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="63f44-132">MOF</span><span class="sxs-lookup"><span data-stu-id="63f44-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63f44-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63f44-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63f44-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63f44-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63f44-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63f44-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63f44-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63f44-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f44-137">**MSVM \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="63f44-137">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




