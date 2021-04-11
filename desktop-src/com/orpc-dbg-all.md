---
title: Structure ORPC_DBG_ALL
description: La \_ structure ORPC dbg \_ All est utilisée pour passer des paramètres aux méthodes de l’interface IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- Structure COM ORPC_DBG_ALL
- Pointeur de structure LPORPC_DBG_ALL COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103260"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="85a66-105">ORPC \_ dbg \_ tout (structure)</span><span class="sxs-lookup"><span data-stu-id="85a66-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="85a66-106">La structure **ORPC \_ dbg \_ All** est utilisée pour passer des paramètres aux méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="85a66-107">Chaque méthode de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) utilise une combinaison différente des membres ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="85a66-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="85a66-108">Si un membre n’est pas indiqué comme utilisé par une méthode, il n’est pas défini lorsqu’il est passé à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="85a66-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85a66-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85a66-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="85a66-110">Membres</span><span class="sxs-lookup"><span data-stu-id="85a66-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="85a66-111">**pSignature**</span><span class="sxs-lookup"><span data-stu-id="85a66-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-112">Pointeur vers une mémoire tampon d' **octets** qui contient :</span><span class="sxs-lookup"><span data-stu-id="85a66-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="85a66-113">Quatre premiers octets : caractères ASCII « MARB » dans l’ordre de mémoire plus élevé.</span><span class="sxs-lookup"><span data-stu-id="85a66-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="85a66-114">16 octets suivants : **GUID** qui identifie la notification appelée.</span><span class="sxs-lookup"><span data-stu-id="85a66-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="85a66-115">Il contient l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="85a66-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="85a66-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="85a66-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="85a66-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="85a66-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="85a66-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="85a66-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="85a66-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="85a66-122">Quatre octets suivants : réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85a66-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-123">Utilisé par toutes les méthodes de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-124">**pMessage**</span><span class="sxs-lookup"><span data-stu-id="85a66-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-125">Pointeur vers une structure [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) qui contient des informations de marshaling de données RPC.</span><span class="sxs-lookup"><span data-stu-id="85a66-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-126">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-127">**REFIID**</span><span class="sxs-lookup"><span data-stu-id="85a66-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-128">Pointeur vers l’IID de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-129">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-130">**pChannel**</span><span class="sxs-lookup"><span data-stu-id="85a66-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-131">Pointeur vers l’interface [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) de l’implémentation du canal RPC com sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="85a66-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-132">Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-133">**pUnkProxyMgr**</span><span class="sxs-lookup"><span data-stu-id="85a66-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-134">Pointeur vers l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de l’objet impliqué dans l’appel de ce débogueur.</span><span class="sxs-lookup"><span data-stu-id="85a66-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="85a66-135">Peut avoir la **valeur null**, mais cela réduit la fonctionnalité du débogueur.</span><span class="sxs-lookup"><span data-stu-id="85a66-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-136">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)et [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-137">**pInterface**</span><span class="sxs-lookup"><span data-stu-id="85a66-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-138">Pointeur vers l’interface COM de la méthode qui sera appelée par ce RPC.</span><span class="sxs-lookup"><span data-stu-id="85a66-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="85a66-139">Ne doit pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="85a66-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-140">Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-141">**pUnkObject**</span><span class="sxs-lookup"><span data-stu-id="85a66-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-142">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="85a66-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-143">Utilisé par les méthodes [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-144">**signé**</span><span class="sxs-lookup"><span data-stu-id="85a66-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-145">L’objectif de ce membre change pour chacune des notifications ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="85a66-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="85a66-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): nombre d’octets que le débogueur client transmet au débogueur de serveur.</span><span class="sxs-lookup"><span data-stu-id="85a66-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="85a66-147">Si la valeur est zéro, aucune information n’est transmise.</span><span class="sxs-lookup"><span data-stu-id="85a66-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="85a66-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** du dernier RPC.</span><span class="sxs-lookup"><span data-stu-id="85a66-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="85a66-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): nombre d’octets que le débogueur client transmet au débogueur de serveur.</span><span class="sxs-lookup"><span data-stu-id="85a66-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="85a66-150">Si la valeur est zéro, aucune information n’est transmise.</span><span class="sxs-lookup"><span data-stu-id="85a66-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-151">Utilisé par les méthodes [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)et [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-152">**pvBuffer**</span><span class="sxs-lookup"><span data-stu-id="85a66-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-153">Pointeur vers une structure [**de \_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md) qui contient les informations de débogage RPC marshalées.</span><span class="sxs-lookup"><span data-stu-id="85a66-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="85a66-154">N’est pas défini si **cbBuffer** est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="85a66-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-155">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-156">**cbBuffer**</span><span class="sxs-lookup"><span data-stu-id="85a66-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-157">Longueur, en octets, des données vers lesquelles pointe **pvBuffer**.</span><span class="sxs-lookup"><span data-stu-id="85a66-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-158">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)et [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-159">**lpcbBuffer**</span><span class="sxs-lookup"><span data-stu-id="85a66-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-160">Nombre d’octets que le débogueur client transmet au débogueur de serveur.</span><span class="sxs-lookup"><span data-stu-id="85a66-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="85a66-161">Si la valeur est zéro, aucune information n’est transmise.</span><span class="sxs-lookup"><span data-stu-id="85a66-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="85a66-162">Cette valeur remplace la valeur retournée dans **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="85a66-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="85a66-163">Utilisé par les méthodes [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="85a66-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="85a66-164">**réservé**</span><span class="sxs-lookup"><span data-stu-id="85a66-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="85a66-165">Réservé.</span><span class="sxs-lookup"><span data-stu-id="85a66-165">Reserved.</span></span> <span data-ttu-id="85a66-166">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="85a66-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85a66-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85a66-167">Requirements</span></span>



| <span data-ttu-id="85a66-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85a66-168">Requirement</span></span> | <span data-ttu-id="85a66-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a66-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="85a66-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85a66-170">Minimum supported client</span></span><br/> | <span data-ttu-id="85a66-171">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85a66-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="85a66-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85a66-172">Minimum supported server</span></span><br/> | <span data-ttu-id="85a66-173">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85a66-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="85a66-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="85a66-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="85a66-175"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="85a66-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a66-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85a66-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a66-177">**\_ \_ mémoire tampon dbg ORPC**</span><span class="sxs-lookup"><span data-stu-id="85a66-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="85a66-178">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="85a66-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="85a66-179">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="85a66-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="85a66-180">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="85a66-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

