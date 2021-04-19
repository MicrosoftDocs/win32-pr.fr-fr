---
description: Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538097"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="1da2b-103">SetAsyncTraceParamsEx fonction)</span><span class="sxs-lookup"><span data-stu-id="1da2b-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="1da2b-104">Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="1da2b-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1da2b-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="1da2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1da2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da2b-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="1da2b-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="1da2b-108">Nom du module associé à la trace.</span><span class="sxs-lookup"><span data-stu-id="1da2b-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="1da2b-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="1da2b-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="1da2b-110">Nom du fichier source qui contient l’exception.</span><span class="sxs-lookup"><span data-stu-id="1da2b-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="1da2b-111">*Tâche*</span><span class="sxs-lookup"><span data-stu-id="1da2b-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="1da2b-112">Numéro de ligne de l’exception dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="1da2b-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="1da2b-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="1da2b-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="1da2b-114">Nom de fonction de l’exception.</span><span class="sxs-lookup"><span data-stu-id="1da2b-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="1da2b-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="1da2b-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="1da2b-116">Constante d’indicateur de trace qui représente l’un des types de suivi disponibles.</span><span class="sxs-lookup"><span data-stu-id="1da2b-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="1da2b-117">Ce paramètre peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1da2b-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1da2b-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Erreur irrécupérable \_ \_Masque de trace** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1da2b-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Erreur \_ \_Masque de trace** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1da2b-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Débogage \_ \_Masque de trace** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="1da2b-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**État \_ \_Masque de trace** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="1da2b-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**\_ FUNCT \_Masque de trace** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="1da2b-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Message \_ \_Masque de trace** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="1da2b-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="1da2b-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Tout \_ \_Masque de trace** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="1da2b-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da2b-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1da2b-125">Return value</span></span>

<span data-ttu-id="1da2b-126">Cette fonction retourne 1 si la fonction est réussie ; Sinon, elle retourne 0.</span><span class="sxs-lookup"><span data-stu-id="1da2b-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da2b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1da2b-127">Remarks</span></span>

<span data-ttu-id="1da2b-128">Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="1da2b-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="1da2b-129">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1da2b-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da2b-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1da2b-130">Requirements</span></span>



| <span data-ttu-id="1da2b-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1da2b-131">Requirement</span></span> | <span data-ttu-id="1da2b-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1da2b-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da2b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1da2b-133">DLL</span></span><br/> | <dl> <span data-ttu-id="1da2b-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1da2b-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
