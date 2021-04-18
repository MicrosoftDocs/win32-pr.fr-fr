---
description: Récupère un identificateur de code d’erreur (IDA) et une chaîne de message non mise en forme lorsqu’une erreur jet est fournie.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532735"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="c5b8c-103">JetErrRawMessage fonction)</span><span class="sxs-lookup"><span data-stu-id="c5b8c-103">JetErrRawMessage function</span></span>

<span data-ttu-id="c5b8c-104">Récupère un identificateur de code d’erreur (IDA) et une chaîne de message non mise en forme lorsqu’une erreur jet est fournie.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b8c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5b8c-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="c5b8c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5b8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b8c-107">*Raise*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-108">Erreur Jet qui correspond aux informations obtenues.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-109">*pIda*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-110">Pointeur vers IDA.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-112">Pointeur vers le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-113">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-114">Nombre d’octets dans le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-116">Pointeur vers le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-117">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-118">Pointeur vers l’identificateur de contexte qui est associé au fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="c5b8c-119">*pwszHelp/fichier*</span><span class="sxs-lookup"><span data-stu-id="c5b8c-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b8c-120">Pointe vers un pointeur vers le fichier qui explique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b8c-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5b8c-121">Return value</span></span>

<span data-ttu-id="c5b8c-122">Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message d’erreur non mis en forme qui indique la raison spécifique de l’échec.</span><span class="sxs-lookup"><span data-stu-id="c5b8c-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b8c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c5b8c-123">Remarks</span></span>

<span data-ttu-id="c5b8c-124">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c5b8c-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b8c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5b8c-125">Requirements</span></span>



| <span data-ttu-id="c5b8c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5b8c-126">Requirement</span></span> | <span data-ttu-id="c5b8c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5b8c-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b8c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b8c-128">DLL</span></span><br/> | <dl> <span data-ttu-id="c5b8c-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b8c-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
