---
description: La fonction CreateHandoffTable crée une table de remise qui comprend les informations du jeu de remise stockées dans le fichier INI de l’analyseur.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: CreateHandoffTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517692"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="3f2fd-103">CreateHandoffTable fonction)</span><span class="sxs-lookup"><span data-stu-id="3f2fd-103">CreateHandoffTable function</span></span>

<span data-ttu-id="3f2fd-104">La fonction **CreateHandoffTable** crée une [*table de remise*](h.md) qui comprend les informations du jeu de remise stockées dans le fichier ini de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f2fd-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="3f2fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f2fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f2fd-107">*CNAME* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2fd-108">Chaîne qui indique la section du fichier INI où se trouvent les informations sur le jeu de remise.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="3f2fd-109">*Inifile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2fd-110">Chaîne qui comprend le nom du fichier INI de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="3f2fd-111">*htable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2fd-112">Handle vers une structure **HANDOFFTABLE** créée et gérée par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="3f2fd-113">*nMaxProtocolEntries* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2fd-114">Nombre qui spécifie le nombre maximal d’entrées que la table de remise peut traiter.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="3f2fd-115">de *base* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f2fd-116">Base numérique des numéros des jeux de remise stockés dans le fichier INI.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f2fd-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3f2fd-117">Return value</span></span>

<span data-ttu-id="3f2fd-118">Si la fonction réussit, la valeur de retour est le nombre d’entrées dans la table de remise.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="3f2fd-119">Si la fonction échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2fd-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3f2fd-120">Remarks</span></span>

<span data-ttu-id="3f2fd-121">La table de remise créée par Moniteur réseau est basée sur les informations fournies dans le fichier INI de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="3f2fd-122">Le handle retourné à la table de remise peut ensuite être utilisé pour obtenir un handle vers l’un des protocoles inclus dans la table.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="3f2fd-123">Pour obtenir un handle de l’un de ces protocoles, appelez [GetProtocolFromTable](getprotocolfromtable.md).</span><span class="sxs-lookup"><span data-stu-id="3f2fd-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="3f2fd-124">Notez que l’application de l’analyseur n’accède jamais directement à la structure **HANDOFFTABLE** .</span><span class="sxs-lookup"><span data-stu-id="3f2fd-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="3f2fd-125">Cette structure est créée et gérée par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="3f2fd-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f2fd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f2fd-126">Requirements</span></span>



| <span data-ttu-id="3f2fd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f2fd-127">Requirement</span></span> | <span data-ttu-id="3f2fd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f2fd-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2fd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f2fd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3f2fd-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3f2fd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f2fd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3f2fd-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f2fd-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3f2fd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f2fd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f2fd-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f2fd-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3f2fd-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f2fd-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f2fd-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f2fd-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f2fd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3f2fd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f2fd-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f2fd-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2fd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f2fd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2fd-140">GetProtocolFromTable</span><span class="sxs-lookup"><span data-stu-id="3f2fd-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="3f2fd-141">HANDOFFTABLE</span><span class="sxs-lookup"><span data-stu-id="3f2fd-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




