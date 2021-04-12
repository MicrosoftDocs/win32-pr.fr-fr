---
description: Récupère des données à partir des entrées spécifiées appartenant à une entrée EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392939"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="f2d74-103">SdbQueryDataExTagID fonction)</span><span class="sxs-lookup"><span data-stu-id="f2d74-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="f2d74-104">Récupère des données à partir des entrées spécifiées appartenant à une entrée EXE.</span><span class="sxs-lookup"><span data-stu-id="f2d74-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2d74-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="f2d74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2d74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d74-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="f2d74-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="f2d74-109">*tiExe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-110">[**TagId**](tagid.md) de l’entrée exe.</span><span class="sxs-lookup"><span data-stu-id="f2d74-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="f2d74-111">*lpszDataName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-112">Nom de l’entrée de données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f2d74-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="f2d74-113">Pour spécifier plusieurs entrées, séparez les noms par des barres obliques inverses (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="f2d74-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="f2d74-114">Si ce paramètre a la **valeur null**, la fonction tente de retourner toutes les entrées de données.</span><span class="sxs-lookup"><span data-stu-id="f2d74-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="f2d74-115">*lpdwDataType* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-116">Type de données des entrées retournées.</span><span class="sxs-lookup"><span data-stu-id="f2d74-116">The data type of the returned entries.</span></span> <span data-ttu-id="f2d74-117">Ce paramètre peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f2d74-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="f2d74-118">**\_fichier binaire reg**</span><span class="sxs-lookup"><span data-stu-id="f2d74-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="f2d74-119">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f2d74-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="f2d74-120">**REG \_ multiple \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="f2d74-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="f2d74-121">**REG \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="f2d74-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="f2d74-122">**\_q QWord**</span><span class="sxs-lookup"><span data-stu-id="f2d74-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="f2d74-123">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="f2d74-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f2d74-124">*lpBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-125">Mémoire tampon qui reçoit les données.</span><span class="sxs-lookup"><span data-stu-id="f2d74-125">The buffer that receives the data.</span></span> <span data-ttu-id="f2d74-126">Si la mémoire tampon n’est pas assez grande pour contenir les données, la fonction échoue et retourne une **\_ \_ mémoire tampon insuffisante**.</span><span class="sxs-lookup"><span data-stu-id="f2d74-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="f2d74-127">*lpcbBufferSize* \[ in, out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-128">Taille de la mémoire tampon *lpBuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="f2d74-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f2d74-129">*ptiData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2d74-130">[**TagId**](tagid.md) de l’entrée de données.</span><span class="sxs-lookup"><span data-stu-id="f2d74-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2d74-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2d74-131">Return value</span></span>

<span data-ttu-id="f2d74-132">Cette fonction retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f2d74-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="f2d74-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f2d74-133">Return code</span></span>                                                                                                    | <span data-ttu-id="f2d74-134">Description</span><span class="sxs-lookup"><span data-stu-id="f2d74-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2d74-135"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="f2d74-136">Un ou plusieurs paramètres d’entrée sont incorrects.</span><span class="sxs-lookup"><span data-stu-id="f2d74-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="f2d74-137"><dt>**ERREUR d’altération de la \_ \_ base de DB interne \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="f2d74-138">Aucune entrée de données n’a été trouvée pour l’entrée EXE.</span><span class="sxs-lookup"><span data-stu-id="f2d74-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="f2d74-139"><dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="f2d74-140">La mémoire tampon n’est pas assez grande pour contenir les entrées de données.</span><span class="sxs-lookup"><span data-stu-id="f2d74-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="f2d74-141"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="f2d74-142">L’allocation de mémoire a échoué.</span><span class="sxs-lookup"><span data-stu-id="f2d74-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="f2d74-143"><dt>**ERREUR \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="f2d74-144">Une entrée de données portant le nom *lpszDataName* est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f2d74-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="f2d74-145"><dt>**ERREUR de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="f2d74-146">La fonction s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f2d74-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="f2d74-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2d74-147">Requirements</span></span>



| <span data-ttu-id="f2d74-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2d74-148">Requirement</span></span> | <span data-ttu-id="f2d74-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2d74-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d74-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2d74-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f2d74-151">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f2d74-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2d74-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f2d74-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2d74-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f2d74-154">DLL</span><span class="sxs-lookup"><span data-stu-id="f2d74-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2d74-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2d74-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




