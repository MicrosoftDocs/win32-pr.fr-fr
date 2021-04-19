---
description: Charge le fichier ruche de Registre spécifié en mémoire et valide la ruche.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: OROpenHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545944"
---
# <a name="oropenhive-function"></a><span data-ttu-id="713f5-103">OROpenHive fonction)</span><span class="sxs-lookup"><span data-stu-id="713f5-103">OROpenHive function</span></span>

<span data-ttu-id="713f5-104">Charge le fichier ruche de Registre spécifié en mémoire et valide la ruche.</span><span class="sxs-lookup"><span data-stu-id="713f5-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="713f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="713f5-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="713f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="713f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713f5-107">*lpHivePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="713f5-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713f5-108">Pointeur vers une chaîne Unicode qui spécifie le nom du fichier ruche du Registre à charger en mémoire.</span><span class="sxs-lookup"><span data-stu-id="713f5-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="713f5-109">Il peut s’agir d’un fichier Hive qui a été enregistré avec la fonction [**ORSaveHive**](orsavehive.md) ou créé avec la fonction [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) .</span><span class="sxs-lookup"><span data-stu-id="713f5-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="713f5-110">La taille du fichier doit être inférieure à 4 Go, et l’appelant doit disposer \_ d’un \_ accès aux données en lecture du fichier.</span><span class="sxs-lookup"><span data-stu-id="713f5-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="713f5-111">Pour plus d’informations, consultez [sécurité des fichiers et droits d’accès](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="713f5-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="713f5-112">*phkResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="713f5-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="713f5-113">Pointeur vers une variable qui reçoit un handle vers la clé racine de la ruche de Registre hors connexion chargée.</span><span class="sxs-lookup"><span data-stu-id="713f5-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="713f5-114">Si le fichier ruche du registre ne peut pas être ouvert ou si la validation échoue, la fonction affecte la **valeur null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="713f5-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713f5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="713f5-115">Return value</span></span>

<span data-ttu-id="713f5-116">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="713f5-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="713f5-117">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="713f5-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="713f5-118">Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="713f5-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="713f5-119">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="713f5-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="713f5-120">Si la taille du fichier est vide ou supérieure à 4 Go, la fonction retourne l’erreur \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="713f5-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="713f5-121">Si l’appelant ne dispose pas des droits d’accès nécessaires pour ouvrir le fichier, la fonction retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="713f5-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="713f5-122">Si la ruche du Registre échoue à la validation, la fonction retourne l’erreur \_ non \_ fichier du Registre \_ .</span><span class="sxs-lookup"><span data-stu-id="713f5-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="713f5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="713f5-123">Remarks</span></span>

<span data-ttu-id="713f5-124">La fonction **OROpenHive** est la seule fonction de Registre hors connexion qui valide une ruche de registre.</span><span class="sxs-lookup"><span data-stu-id="713f5-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="713f5-125">Si la validation échoue, aucune tentative n’est faite pour réparer la ruche.</span><span class="sxs-lookup"><span data-stu-id="713f5-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="713f5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="713f5-126">Requirements</span></span>



| <span data-ttu-id="713f5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="713f5-127">Requirement</span></span> | <span data-ttu-id="713f5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="713f5-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="713f5-129">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="713f5-129">Redistributable</span></span><br/> | <span data-ttu-id="713f5-130">Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="713f5-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="713f5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="713f5-131">Header</span></span><br/>          | <dl> <span data-ttu-id="713f5-132"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="713f5-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="713f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="713f5-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="713f5-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="713f5-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="713f5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="713f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713f5-136">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="713f5-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="713f5-137">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="713f5-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="713f5-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="713f5-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="713f5-139">RegSaveKey</span><span class="sxs-lookup"><span data-stu-id="713f5-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="713f5-140">RegSaveKeyEx</span><span class="sxs-lookup"><span data-stu-id="713f5-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
