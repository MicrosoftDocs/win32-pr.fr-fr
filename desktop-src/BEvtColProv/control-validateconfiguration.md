---
description: Validez un texte de configuration pour l’exactitude sans le définir comme actif. Retourne 1 en cas de réussite, 0 en cas d’erreur.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Méthode ValidateConfiguration de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950405"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="b3db6-104">Méthode ValidateConfiguration de la classe Control</span><span class="sxs-lookup"><span data-stu-id="b3db6-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="b3db6-105">Validez un texte de configuration pour l’exactitude sans le définir comme actif.</span><span class="sxs-lookup"><span data-stu-id="b3db6-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="b3db6-106">Retourne 1 en cas de réussite, 0 en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3db6-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3db6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3db6-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="b3db6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3db6-109">*Configuration* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-110">Configuration à vérifier.</span><span class="sxs-lookup"><span data-stu-id="b3db6-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-111">*ErrorString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-112">Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre contient une description de l’erreur de validation pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b3db6-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-113">*WarningString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-114">Lorsque cette méthode est retournée, ce paramètre contient une description de tous les avertissements de validation pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="b3db6-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="b3db6-115">Chaîne de texte avec des avertissements.</span><span class="sxs-lookup"><span data-stu-id="b3db6-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-116">*InfoString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-117">Lorsque cette méthode est retournée, ce paramètre contient un ensemble d’informations sur la configuration.</span><span class="sxs-lookup"><span data-stu-id="b3db6-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-118">*ErrorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-119">Lorsque cette méthode est retournée, si une erreur de validation s’est produite, ce paramètre indique le type d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b3db6-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="b3db6-120">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3db6-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="b3db6-121">0</span><span class="sxs-lookup"><span data-stu-id="b3db6-121">0</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-122">L’argument est manquant.</span><span class="sxs-lookup"><span data-stu-id="b3db6-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-123">1</span><span class="sxs-lookup"><span data-stu-id="b3db6-123">1</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-124">Le format de l’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b3db6-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="b3db6-125">2</span><span class="sxs-lookup"><span data-stu-id="b3db6-125">2</span></span>
</dt> <dd>

<span data-ttu-id="b3db6-126">Un argument de configuration n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b3db6-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3db6-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3db6-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="b3db6-128">0</span><span class="sxs-lookup"><span data-stu-id="b3db6-128">0</span></span>

<span data-ttu-id="b3db6-129">Échec</span><span class="sxs-lookup"><span data-stu-id="b3db6-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b3db6-130">1</span><span class="sxs-lookup"><span data-stu-id="b3db6-130">1</span></span>

<span data-ttu-id="b3db6-131">Succès</span><span class="sxs-lookup"><span data-stu-id="b3db6-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3db6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3db6-132">Requirements</span></span>



| <span data-ttu-id="b3db6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3db6-133">Requirement</span></span> | <span data-ttu-id="b3db6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3db6-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3db6-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3db6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3db6-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3db6-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b3db6-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3db6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3db6-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b3db6-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="b3db6-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3db6-139">Namespace</span></span><br/>                | <span data-ttu-id="b3db6-140">Racine \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="b3db6-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="b3db6-141">MOF</span><span class="sxs-lookup"><span data-stu-id="b3db6-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3db6-142"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3db6-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3db6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b3db6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3db6-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3db6-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b3db6-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3db6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3db6-146">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="b3db6-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




