---
description: Récupère un identificateur de code d’erreur (IDA) et crée la dernière chaîne d’affichage lorsqu’une erreur jet et des informations d’erreur étendues sont fournies.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541264"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="641aa-103">JetErrFormattedMessage fonction)</span><span class="sxs-lookup"><span data-stu-id="641aa-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="641aa-104">Récupère un identificateur de code d’erreur (IDA) et crée la dernière chaîne d’affichage lorsqu’une erreur jet et des informations d’erreur étendues sont fournies.</span><span class="sxs-lookup"><span data-stu-id="641aa-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="641aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="641aa-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="641aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="641aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="641aa-107">*Raise*</span><span class="sxs-lookup"><span data-stu-id="641aa-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-108">Numéro d’erreur jet utilisé pour rechercher et mettre en forme le message d’erreur affichable.</span><span class="sxs-lookup"><span data-stu-id="641aa-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-109">*pExtendedErrorInfo*</span><span class="sxs-lookup"><span data-stu-id="641aa-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-110">Toutes les informations sur les erreurs jet, y compris le nom de la base de données, le nom de la table et toute information d’erreur mineure.</span><span class="sxs-lookup"><span data-stu-id="641aa-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-111">*pIda*</span><span class="sxs-lookup"><span data-stu-id="641aa-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-112">Pointeur vers IDA associé au code d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="641aa-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="641aa-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-114">Pointeur vers le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="641aa-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-115">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="641aa-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-116">Nombre d’octets dans le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="641aa-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="641aa-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-118">Pointeur vers le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="641aa-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-119">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="641aa-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-120">Pointeur vers l’identificateur de contexte qui est associé au fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="641aa-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="641aa-121">*pwszHelp/fichier*</span><span class="sxs-lookup"><span data-stu-id="641aa-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="641aa-122">Pointeur vers un pointeur vers le fichier qui explique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="641aa-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="641aa-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="641aa-123">Return value</span></span>

<span data-ttu-id="641aa-124">Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message d’erreur mis en forme qui indique la raison spécifique de l’échec.</span><span class="sxs-lookup"><span data-stu-id="641aa-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="641aa-125">Notes</span><span class="sxs-lookup"><span data-stu-id="641aa-125">Remarks</span></span>

<span data-ttu-id="641aa-126">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="641aa-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="641aa-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="641aa-127">Requirements</span></span>



| <span data-ttu-id="641aa-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="641aa-128">Requirement</span></span> | <span data-ttu-id="641aa-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="641aa-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="641aa-130">DLL</span><span class="sxs-lookup"><span data-stu-id="641aa-130">DLL</span></span><br/> | <dl> <span data-ttu-id="641aa-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="641aa-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
