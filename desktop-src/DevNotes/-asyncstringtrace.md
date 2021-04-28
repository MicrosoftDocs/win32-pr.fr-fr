---
description: 'Fonction AsyncStringTrace : termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style sprintf.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085797"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="348a2-103">AsyncStringTrace fonction)</span><span class="sxs-lookup"><span data-stu-id="348a2-103">AsyncStringTrace function</span></span>

<span data-ttu-id="348a2-104">Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="348a2-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="348a2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="348a2-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="348a2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="348a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="348a2-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="348a2-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="348a2-108">Paramètre de trace 32 bits utilisé pour le filtrage au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="348a2-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="348a2-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="348a2-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="348a2-110">Chaîne se terminant par zéro qui décrit le format de la trace.</span><span class="sxs-lookup"><span data-stu-id="348a2-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="348a2-111">*repère*</span><span class="sxs-lookup"><span data-stu-id="348a2-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="348a2-112">Marqueur pour les fonctions **vsprintf** .</span><span class="sxs-lookup"><span data-stu-id="348a2-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="348a2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="348a2-113">Return value</span></span>

<span data-ttu-id="348a2-114">Cette fonction retourne la longueur de l’instruction de trace, en octets.</span><span class="sxs-lookup"><span data-stu-id="348a2-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="348a2-115">Notes </span><span class="sxs-lookup"><span data-stu-id="348a2-115">Remarks</span></span>

<span data-ttu-id="348a2-116">Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="348a2-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="348a2-117">Le type de données de la **\_ liste va** est un type standard utilisé pour stocker les informations requises par les macros End **\_ arg** et **va \_ end** .</span><span class="sxs-lookup"><span data-stu-id="348a2-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="348a2-118">Pour plus d’informations, consultez [types standard](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="348a2-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="348a2-119">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="348a2-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="348a2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="348a2-120">Requirements</span></span>



| <span data-ttu-id="348a2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="348a2-121">Requirement</span></span> | <span data-ttu-id="348a2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="348a2-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="348a2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="348a2-123">DLL</span></span><br/> | <dl> <span data-ttu-id="348a2-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="348a2-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

