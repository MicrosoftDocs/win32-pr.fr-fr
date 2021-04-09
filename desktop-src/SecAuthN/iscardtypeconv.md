---
description: Fournit les méthodes nécessaires pour prendre en charge les utilisateurs des autres interfaces COM de carte à puce.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interface ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865038"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="bfd96-103">Interface ISCardTypeConv</span><span class="sxs-lookup"><span data-stu-id="bfd96-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="bfd96-104">\[L’interface **ISCardTypeConv** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bfd96-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bfd96-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bfd96-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bfd96-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bfd96-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bfd96-107">L’interface **ISCardTypeConv** fournit les méthodes nécessaires pour prendre en charge les utilisateurs des autres interfaces COM de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd96-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="bfd96-108">Cette interface n’est fournie qu’à des fins de compatibilité descendante et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="bfd96-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="bfd96-109">Membres</span><span class="sxs-lookup"><span data-stu-id="bfd96-109">Members</span></span>

<span data-ttu-id="bfd96-110">L’interface **ISCardTypeConv** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bfd96-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bfd96-111">**ISCardTypeConv** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bfd96-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="bfd96-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bfd96-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bfd96-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bfd96-113">Methods</span></span>

<span data-ttu-id="bfd96-114">L’interface **ISCardTypeConv** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bfd96-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="bfd96-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="bfd96-115">Method</span></span>                                                                              | <span data-ttu-id="bfd96-116">Description</span><span class="sxs-lookup"><span data-stu-id="bfd96-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfd96-117">**ConvertByteArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="bfd96-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="bfd96-118">Convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="bfd96-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="bfd96-119">**ConvertByteBufferToByteArray**</span><span class="sxs-lookup"><span data-stu-id="bfd96-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="bfd96-120">Convertit un tableau d’octets mappé dans une mémoire tampon universelle d’octets (objet **IStream** ) en un tableau d’octets C/C++ classique.</span><span class="sxs-lookup"><span data-stu-id="bfd96-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="bfd96-121">**ConvertByteBufferToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="bfd96-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="bfd96-122">Convertit un tableau d’octets mappé dans une mémoire tampon universelle d’octets (objet **IStream** ) en un SafeArray de type non signé (Byte).</span><span class="sxs-lookup"><span data-stu-id="bfd96-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="bfd96-123">**ConvertSafeArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="bfd96-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="bfd96-124">Convertit un tableau d’octets défini en tant que SAFEARRAY en une mémoire tampon universelle d’octets (objet **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="bfd96-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="bfd96-125">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="bfd96-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="bfd96-126">Crée un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="bfd96-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="bfd96-127">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="bfd96-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="bfd96-128">Crée une mémoire tampon universelle d’octets mappés à un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="bfd96-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="bfd96-129">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="bfd96-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="bfd96-130">Crée un SAFEARRAY Automation de caractères non signés (octets).</span><span class="sxs-lookup"><span data-stu-id="bfd96-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="bfd96-131">**FreeIStreamMemoryPtr**</span><span class="sxs-lookup"><span data-stu-id="bfd96-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="bfd96-132">Libère un pointeur de mémoire vers le bloc de mémoire HGLOBAL géré par une interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="bfd96-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="bfd96-133">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="bfd96-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="bfd96-134">Acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="bfd96-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="bfd96-135">**SizeOfIStream**</span><span class="sxs-lookup"><span data-stu-id="bfd96-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="bfd96-136">Détermine la taille (nombre d’octets) d’une interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="bfd96-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="bfd96-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfd96-137">Requirements</span></span>



| <span data-ttu-id="bfd96-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfd96-138">Requirement</span></span> | <span data-ttu-id="bfd96-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfd96-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd96-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd96-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd96-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfd96-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bfd96-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfd96-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd96-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfd96-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bfd96-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bfd96-144">End of client support</span></span><br/>    | <span data-ttu-id="bfd96-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfd96-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bfd96-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bfd96-146">End of server support</span></span><br/>    | <span data-ttu-id="bfd96-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfd96-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bfd96-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfd96-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd96-149"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd96-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfd96-150">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bfd96-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfd96-151"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfd96-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfd96-152">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd96-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd96-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd96-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfd96-154">IID</span><span class="sxs-lookup"><span data-stu-id="bfd96-154">IID</span></span><br/>                      | <span data-ttu-id="bfd96-155">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bfd96-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
