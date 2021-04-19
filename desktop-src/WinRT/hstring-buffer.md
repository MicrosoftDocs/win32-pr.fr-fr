---
description: Handle vers une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514022"
---
# <a name="hstring_buffer"></a><span data-ttu-id="956b2-103">\_mémoire tampon HSTRING</span><span class="sxs-lookup"><span data-stu-id="956b2-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="956b2-104">Handle vers une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un [**HSTRING**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="956b2-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="956b2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="956b2-105">Remarks</span></span>

<span data-ttu-id="956b2-106">**HSTRING \_ BUFFER** représente une mémoire tampon de chaîne que vous pouvez modifier avant de la convertir en [**HSTRING**](hstring.md)immuable.</span><span class="sxs-lookup"><span data-stu-id="956b2-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="956b2-107">Appelez la fonction [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) pour créer une **\_ mémoire tampon HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="956b2-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="956b2-108">Appelez [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) pour convertir une **\_ mémoire tampon HSTRING** en un [**HSTRING**](hstring.md)immuable.</span><span class="sxs-lookup"><span data-stu-id="956b2-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="956b2-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="956b2-109">Requirements</span></span>



| <span data-ttu-id="956b2-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="956b2-110">Requirement</span></span> | <span data-ttu-id="956b2-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="956b2-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="956b2-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="956b2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="956b2-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="956b2-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="956b2-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="956b2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="956b2-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="956b2-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="956b2-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="956b2-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="956b2-117"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956b2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="956b2-118">See also</span></span>

<dl> <span data-ttu-id="956b2-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="956b2-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="956b2-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="956b2-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="956b2-121">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="956b2-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="956b2-122">**WindowsPromoteStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="956b2-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
