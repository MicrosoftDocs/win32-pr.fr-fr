---
description: Récupère l’état du cache de Fichiers hors connexion.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541455"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="41459-103">CSCQueryDatabaseStatus fonction)</span><span class="sxs-lookup"><span data-stu-id="41459-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="41459-104">\[Cette fonction n’est pas prise en charge et ne doit pas être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="41459-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="41459-105">Récupère l’état du cache de Fichiers hors connexion.</span><span class="sxs-lookup"><span data-stu-id="41459-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="41459-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41459-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="41459-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41459-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41459-108">*pulStatus*</span><span class="sxs-lookup"><span data-stu-id="41459-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="41459-109">Statut.</span><span class="sxs-lookup"><span data-stu-id="41459-109">The status.</span></span> <span data-ttu-id="41459-110">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="41459-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="41459-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="41459-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="41459-112">Signification</span><span class="sxs-lookup"><span data-stu-id="41459-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="41459-113"><dt>**Indicateur \_ DATABASESTATUS \_ chiffré**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="41459-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="41459-114">Le cache est marqué pour le chiffrement et tous les fichiers du cache sont chiffrés.</span><span class="sxs-lookup"><span data-stu-id="41459-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="41459-115"><dt>**Indicateur \_ DATABASESTATUS \_ partiellement \_ chiffré**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="41459-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="41459-116">Le cache est marqué pour le chiffrement, mais certains fichiers du cache ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="41459-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="41459-117"><dt>**Indicateur \_ DATABASESTATUS \_ partiellement \_ non chiffré**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="41459-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="41459-118">Le cache n’est pas marqué pour le chiffrement, mais tous les fichiers du cache n’ont pas été déchiffrés.</span><span class="sxs-lookup"><span data-stu-id="41459-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="41459-119"><dt>**Indicateur \_ DATABASESTATUS \_ non chiffré**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="41459-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="41459-120">Le cache n’est pas marqué pour le chiffrement et tous les fichiers du cache ont été déchiffrés.</span><span class="sxs-lookup"><span data-stu-id="41459-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="41459-121">*pulErrors*</span><span class="sxs-lookup"><span data-stu-id="41459-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="41459-122">Ce paramètre est une valeur différente de zéro s’il existe une erreur de base de données interne ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="41459-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41459-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41459-123">Return value</span></span>

<span data-ttu-id="41459-124">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="41459-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="41459-125">Notes</span><span class="sxs-lookup"><span data-stu-id="41459-125">Remarks</span></span>

<span data-ttu-id="41459-126">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="41459-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="41459-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41459-127">Requirements</span></span>



| <span data-ttu-id="41459-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41459-128">Requirement</span></span> | <span data-ttu-id="41459-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="41459-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41459-130">DLL</span><span class="sxs-lookup"><span data-stu-id="41459-130">DLL</span></span><br/> | <dl> <span data-ttu-id="41459-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41459-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41459-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41459-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41459-133">**CSCIsCSCEnabled**</span><span class="sxs-lookup"><span data-stu-id="41459-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
