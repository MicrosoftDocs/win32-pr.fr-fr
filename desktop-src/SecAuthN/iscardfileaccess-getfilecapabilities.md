---
description: La méthode GetFileCapabilities récupère une liste de fonctionnalités de fichier à partir du fichier actif.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'ISCardFileAccess :: GetFileCapabilities, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203567"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="37caa-103">ISCardFileAccess :: GetFileCapabilities, méthode</span><span class="sxs-lookup"><span data-stu-id="37caa-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="37caa-104">\[La méthode **GetFileCapabilities** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="37caa-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="37caa-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="37caa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="37caa-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="37caa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="37caa-107">La méthode **GetFileCapabilities** récupère une liste de fonctionnalités de fichier à partir du fichier actif.</span><span class="sxs-lookup"><span data-stu-id="37caa-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="37caa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37caa-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="37caa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37caa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37caa-110">*ppProperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37caa-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37caa-111">Structures de pointeur vers TLV (balise, longueur, valeur).</span><span class="sxs-lookup"><span data-stu-id="37caa-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="37caa-112">En entrée, ce paramètre indique les fichiers pour lesquels obtenir des propriétés ; lors de la sortie, ce paramètre contient les propriétés.</span><span class="sxs-lookup"><span data-stu-id="37caa-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="37caa-113">L’exemple suivant est une définition de la structure TLV.</span><span class="sxs-lookup"><span data-stu-id="37caa-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="37caa-114">Pour plus d’informations sur les structures TLV, consultez [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="37caa-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="37caa-115">*plProperties* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="37caa-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37caa-116">Pointeur vers le nombre d’entrées TLV dans *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="37caa-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="37caa-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="37caa-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37caa-118">Spécifie si la messagerie sécurisée doit être utilisée et les données préallouées.</span><span class="sxs-lookup"><span data-stu-id="37caa-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="37caa-119">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="37caa-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="37caa-120">**SC \_ FL \_ préalloué**</span><span class="sxs-lookup"><span data-stu-id="37caa-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37caa-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37caa-121">Return value</span></span>

<span data-ttu-id="37caa-122">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="37caa-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="37caa-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="37caa-123">Return code</span></span>                                                                                   | <span data-ttu-id="37caa-124">Description</span><span class="sxs-lookup"><span data-stu-id="37caa-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="37caa-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37caa-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="37caa-126">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="37caa-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="37caa-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="37caa-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="37caa-128">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="37caa-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="37caa-129"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="37caa-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="37caa-130">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="37caa-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="37caa-131"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="37caa-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="37caa-132">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="37caa-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="37caa-133">Notes</span><span class="sxs-lookup"><span data-stu-id="37caa-133">Remarks</span></span>

<span data-ttu-id="37caa-134">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="37caa-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="37caa-135">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="37caa-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="37caa-136">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="37caa-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37caa-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37caa-137">Requirements</span></span>



| <span data-ttu-id="37caa-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37caa-138">Requirement</span></span> | <span data-ttu-id="37caa-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="37caa-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37caa-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37caa-140">Minimum supported client</span></span><br/> | <span data-ttu-id="37caa-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37caa-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="37caa-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37caa-142">Minimum supported server</span></span><br/> | <span data-ttu-id="37caa-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37caa-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="37caa-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="37caa-144">End of client support</span></span><br/>    | <span data-ttu-id="37caa-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="37caa-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="37caa-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="37caa-146">End of server support</span></span><br/>    | <span data-ttu-id="37caa-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37caa-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="37caa-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37caa-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37caa-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="37caa-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
