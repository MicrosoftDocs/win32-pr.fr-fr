---
description: Récupère une chaîne de message non mise en forme lorsqu’un identificateur de code d’erreur (IDA) est fourni.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526643"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="09770-103">JetErrIDARawMessage fonction)</span><span class="sxs-lookup"><span data-stu-id="09770-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="09770-104">Récupère une chaîne de message non mise en forme lorsqu’un identificateur de code d’erreur (IDA) est fourni.</span><span class="sxs-lookup"><span data-stu-id="09770-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="09770-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09770-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="09770-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09770-107">*Ida*</span><span class="sxs-lookup"><span data-stu-id="09770-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-108">Numéro qui mappe à un code d’erreur spécifique et qui est affiché à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09770-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="09770-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="09770-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-110">Pointeur vers le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="09770-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="09770-111">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="09770-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-112">Nombre d’octets dans le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="09770-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="09770-113">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="09770-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-114">Pointeur vers le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="09770-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="09770-115">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="09770-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-116">Pointeur vers l’identificateur de contexte qui est associé au fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="09770-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="09770-117">*pwszHelp/fichier*</span><span class="sxs-lookup"><span data-stu-id="09770-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="09770-118">Pointeur vers un pointeur vers le fichier qui explique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="09770-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09770-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09770-119">Return value</span></span>

<span data-ttu-id="09770-120">Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message sans mise en forme qui indique la raison spécifique de l’échec.</span><span class="sxs-lookup"><span data-stu-id="09770-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="09770-121">Notes</span><span class="sxs-lookup"><span data-stu-id="09770-121">Remarks</span></span>

<span data-ttu-id="09770-122">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="09770-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="09770-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09770-123">Requirements</span></span>



| <span data-ttu-id="09770-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09770-124">Requirement</span></span> | <span data-ttu-id="09770-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="09770-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09770-126">DLL</span><span class="sxs-lookup"><span data-stu-id="09770-126">DLL</span></span><br/> | <dl> <span data-ttu-id="09770-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09770-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
