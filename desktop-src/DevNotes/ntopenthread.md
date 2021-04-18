---
description: Ouvre un handle vers un objet thread avec l’accès spécifié.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540476"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="0ab34-103">NtOpenThread fonction)</span><span class="sxs-lookup"><span data-stu-id="0ab34-103">NtOpenThread function</span></span>

<span data-ttu-id="0ab34-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.</span><span class="sxs-lookup"><span data-stu-id="0ab34-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="0ab34-105">Utilisez à la place la fonction [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]</span><span class="sxs-lookup"><span data-stu-id="0ab34-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="0ab34-106">Ouvre un handle vers un objet thread avec l’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="0ab34-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab34-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ab34-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="0ab34-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ab34-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab34-109">*ThreadHandle* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ab34-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab34-110">Pointeur vers une variable qui reçoit le handle de l’objet thread.</span><span class="sxs-lookup"><span data-stu-id="0ab34-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="0ab34-111">*DesiredAccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab34-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab34-112">Type de données de [**\_ masque d’accès**](../secauthz/access-mask-format.md) qui fournit les types d’accès souhaités pour l’objet thread.</span><span class="sxs-lookup"><span data-stu-id="0ab34-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="0ab34-113">*ObjectAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab34-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab34-114">Pointeur vers une structure [d' \_ attributs d’objet](https://msdn.microsoft.com/library/aa491657.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0ab34-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="0ab34-115">Le membre **ObjectName** de cette structure doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0ab34-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="0ab34-116">**Windows Server 2003 et Windows XP :** Le membre **ObjectName** de cette structure peut pointer vers un nom d’objet.</span><span class="sxs-lookup"><span data-stu-id="0ab34-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="0ab34-117">Si **ObjectName** n’a pas la valeur null, le paramètre *ClientID* doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0ab34-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="0ab34-118">*ClientID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ab34-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab34-119">Pointeur vers une structure **d' \_ ID client** qui identifie le thread dont le thread doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="0ab34-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="0ab34-120">**Windows Server 2003 et Windows XP :** Pointeur vers une structure **d' \_ ID client** qui identifie le thread dont le thread doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="0ab34-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="0ab34-121">Ce paramètre peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="0ab34-121">This parameter can be NULL.</span></span> <span data-ttu-id="0ab34-122">Si ce paramètre n’est pas NULL, le membre **ObjectName** de la structure vers laquelle pointe le paramètre *ObjectAttributes* doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0ab34-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab34-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ab34-123">Return value</span></span>

<span data-ttu-id="0ab34-124">Retourne un code **NTSTATUS** ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0ab34-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="0ab34-125">Les formulaires et la signification des codes d’erreur de **NTSTATUS** sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.</span><span class="sxs-lookup"><span data-stu-id="0ab34-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab34-126">Notes</span><span class="sxs-lookup"><span data-stu-id="0ab34-126">Remarks</span></span>

<span data-ttu-id="0ab34-127">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="0ab34-127">This function has no associated header file.</span></span> <span data-ttu-id="0ab34-128">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="0ab34-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="0ab34-129">Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="0ab34-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab34-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ab34-130">Requirements</span></span>



| <span data-ttu-id="0ab34-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ab34-131">Requirement</span></span> | <span data-ttu-id="0ab34-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ab34-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab34-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0ab34-133">DLL</span></span><br/> | <dl> <span data-ttu-id="0ab34-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ab34-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
