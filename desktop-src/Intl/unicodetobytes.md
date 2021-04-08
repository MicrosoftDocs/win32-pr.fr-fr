---
UID: ''
title: UnicodeToBytes fonction)
description: Convertit les caractères Unicode en octets GB18030.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "103679502"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="7cece-103">UnicodeToBytes fonction)</span><span class="sxs-lookup"><span data-stu-id="7cece-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="7cece-104">Description</span><span class="sxs-lookup"><span data-stu-id="7cece-104">Description</span></span>

<span data-ttu-id="7cece-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7cece-105">Deprecated.</span></span> <span data-ttu-id="7cece-106">Convertit les caractères Unicode en octets GB18030.</span><span class="sxs-lookup"><span data-stu-id="7cece-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="7cece-107">**Remarque**  Lors de la conversion de caractères Unicode en octets GB18030, une application à exécuter sur Windows Vista et les versions ultérieures doit utiliser la fonction [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .</span><span class="sxs-lookup"><span data-stu-id="7cece-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="7cece-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cece-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="7cece-109">lpWideCharStr [in]</span><span class="sxs-lookup"><span data-stu-id="7cece-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="7cece-110">Pointeur vers la chaîne Unicode à convertir.</span><span class="sxs-lookup"><span data-stu-id="7cece-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="7cece-111">cchWideChar [in]</span><span class="sxs-lookup"><span data-stu-id="7cece-111">cchWideChar [in]</span></span>

<span data-ttu-id="7cece-112">Nombre de caractères de la chaîne Unicode à convertir.</span><span class="sxs-lookup"><span data-stu-id="7cece-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="7cece-113">lpMultiByteStr [in]</span><span class="sxs-lookup"><span data-stu-id="7cece-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="7cece-114">Pointeur vers la mémoire tampon multioctet cible.</span><span class="sxs-lookup"><span data-stu-id="7cece-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="7cece-115">Si *lpMultiByteStr* est égal à 0, le nombre d’octets du résultat GB18030 est retourné et aucune conversion n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7cece-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="7cece-116">cchMultiByte [in]</span><span class="sxs-lookup"><span data-stu-id="7cece-116">cchMultiByte [in]</span></span>

<span data-ttu-id="7cece-117">Nombre d’octets de la mémoire tampon multioctets cible.</span><span class="sxs-lookup"><span data-stu-id="7cece-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="7cece-118">Si *cchMultiByte* est égal à 0, le nombre d’octets du résultat GB18030 est retourné et aucune conversion n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7cece-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="7cece-119">Retours</span><span class="sxs-lookup"><span data-stu-id="7cece-119">Returns</span></span>

<span data-ttu-id="7cece-120">Retourne le nombre d’octets des caractères multioctets qui sont générés, en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="7cece-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cece-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7cece-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="7cece-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cece-122">See also</span></span>

[<span data-ttu-id="7cece-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="7cece-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="7cece-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="7cece-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
