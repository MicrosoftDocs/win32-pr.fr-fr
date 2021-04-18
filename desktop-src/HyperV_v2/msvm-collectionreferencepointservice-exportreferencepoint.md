---
description: Exporte une collection de points de référence dans un fichier. La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Méthode ExportReferencePoint de la classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542995"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="ec185-104">Méthode ExportReferencePoint de la \_ classe CollectionReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="ec185-104">ExportReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="ec185-105">Exporte une collection de points de référence dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ec185-105">Exports a reference point collection to a file.</span></span> <span data-ttu-id="ec185-106">La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="ec185-106">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec185-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec185-107">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ec185-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec185-109">*ReferencePointCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec185-109">*ReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec185-110">Référence à une [**\_ collection CIM**](cim-collection.md) qui représente la collection de points de référence à exporter.</span><span class="sxs-lookup"><span data-stu-id="ec185-110">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the reference point collection to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-111">*ExportDirectory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec185-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec185-112">Chemin d’accès complet du répertoire dans lequel la collection de points de référence doit être exportée.</span><span class="sxs-lookup"><span data-stu-id="ec185-112">The fully-qualified path of the directory to which the reference point collection is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-113">*ExportSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ec185-113">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec185-114">Instance de [**MSVM \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) qui représente les paramètres de l’opération d’exportation.</span><span class="sxs-lookup"><span data-stu-id="ec185-114">An instance of [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="ec185-115">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec185-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec185-116">Référence facultative qui est retournée si l’opération est exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ec185-116">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="ec185-117">Si elle est présente, la référence retournée à une instance de [**\_ ConcreteJob CIM**](cim-concretejob.md) peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec185-117">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec185-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec185-118">Return value</span></span>

<span data-ttu-id="ec185-119">Si cette méthode est exécutée de façon synchrone, elle retourne 0 si elle réussit.</span><span class="sxs-lookup"><span data-stu-id="ec185-119">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="ec185-120">Si cette méthode est exécutée de façon asynchrone, elle retourne 4096 et le paramètre de sortie de la tâche peut être utilisé pour suivre la progression de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ec185-120">If this method is executed asynchronously, it returns 4096 and the Job output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="ec185-121">Toute autre valeur de retour indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="ec185-121">Any other return value indicates an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec185-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec185-122">Requirements</span></span>



| <span data-ttu-id="ec185-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec185-123">Requirement</span></span> | <span data-ttu-id="ec185-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec185-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec185-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec185-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec185-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec185-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ec185-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec185-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec185-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ec185-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ec185-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec185-129">Namespace</span></span><br/>                | <span data-ttu-id="ec185-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec185-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec185-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ec185-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec185-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec185-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec185-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ec185-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec185-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec185-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec185-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec185-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec185-136">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="ec185-136">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




