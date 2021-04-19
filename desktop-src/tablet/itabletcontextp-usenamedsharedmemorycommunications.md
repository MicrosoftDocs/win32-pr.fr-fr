---
description: Configure la communication de la mémoire partagée pour le contexte de la tablette.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'ITabletContextP :: UseNamedSharedMemoryCommunications, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544934"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a><span data-ttu-id="1e464-103">ITabletContextP :: UseNamedSharedMemoryCommunications, méthode</span><span class="sxs-lookup"><span data-stu-id="1e464-103">ITabletContextP::UseNamedSharedMemoryCommunications method</span></span>

<span data-ttu-id="1e464-104">Configure la communication de la mémoire partagée pour le contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="1e464-104">Sets up shared memory communication for the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e464-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e464-105">Syntax</span></span>


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a><span data-ttu-id="1e464-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e464-107">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e464-107">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-108">ID de processus du client qui accède à la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-108">The process ID of the client that accesses shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-109">*pszCallerSid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e464-109">*pszCallerSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-110">Identificateur de sécurité de l’appelant de la fonction.</span><span class="sxs-lookup"><span data-stu-id="1e464-110">The security identifier of the function caller.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-111">*pszCallerIntegritySid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e464-111">*pszCallerIntegritySid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-112">Identificateur de sécurité qui peut vérifier l’intégrité de la fonction appelante.</span><span class="sxs-lookup"><span data-stu-id="1e464-112">The security identifier that can verify the integrity of the calling function.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-113">*pdwEventMoreDataId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e464-113">*pdwEventMoreDataId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-114">Entier utilisé pour construire le nom d’un événement.</span><span class="sxs-lookup"><span data-stu-id="1e464-114">An integer used to construct the name of an event.</span></span> <span data-ttu-id="1e464-115">L’événement indique s’il y a plus de données.</span><span class="sxs-lookup"><span data-stu-id="1e464-115">The event indicates whether there is more data.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-116">*pdwEventClientReadyId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e464-116">*pdwEventClientReadyId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-117">Entier utilisé pour construire le nom d’un événement.</span><span class="sxs-lookup"><span data-stu-id="1e464-117">An integer used to construct the name of an event.</span></span> <span data-ttu-id="1e464-118">L’événement signale que le client est prêt à recevoir des données.</span><span class="sxs-lookup"><span data-stu-id="1e464-118">The event signals that the client is ready to receive data.</span></span> <span data-ttu-id="1e464-119">L’événement est signalé après le traitement de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="1e464-119">The event is signaled after processing new data.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-120">*pdwMutexAccessId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e464-120">*pdwMutexAccessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-121">Pointeur vers l’identificateur d’accès de la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-121">A pointer to the access identifier of the shared memory.</span></span>

</dd> <dt>

<span data-ttu-id="1e464-122">*pdwFileMappingId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e464-122">*pdwFileMappingId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e464-123">Entier qui identifie la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-123">An integer that identifies the shared memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e464-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e464-124">Return value</span></span>

<span data-ttu-id="1e464-125">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e464-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e464-126">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e464-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e464-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1e464-127">Remarks</span></span>

<span data-ttu-id="1e464-128">La méthode **UseNamedSharedMemoryCommunications** fait partie du protocole de mémoire partagée du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="1e464-128">The **UseNamedSharedMemoryCommunications** method is part of the Tablet PC shared memory protocol.</span></span> <span data-ttu-id="1e464-129">Un client sans privilèges élevés passe dans un identificateur de sécurité (SID) et un identificateur de sécurité de niveau d’intégrité (IL-SID) afin que le service tablette puisse utiliser des listes de contrôle d’accès (ACL) pour accéder aux objets de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-129">A client without elevated privileges passes in a security identifier (SID) and an integrity level security identifier (IL-SID) so that the Tablet service can use access control lists (ACL) to access the shared memory objects.</span></span> <span data-ttu-id="1e464-130">Si le client dispose de privilèges élevés, il doit utiliser UseSharedMemoryCommunications, qui est l’API appelée si le service a déjà un privilège élevé.</span><span class="sxs-lookup"><span data-stu-id="1e464-130">If the client has elevated privileges, it should use UseSharedMemoryCommunications, which is the API that is called if the service already has an elevated privilege.</span></span>

<span data-ttu-id="1e464-131">La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) stocke l’en-tête de mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-131">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure stores the shared memory header.</span></span>

<span data-ttu-id="1e464-132">La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) est convertie à partir des données référencées par le mappage de fichier.</span><span class="sxs-lookup"><span data-stu-id="1e464-132">The [**SHAREDMEMORY\_HEADER**](sharedmemory-header.md) structure is cast from the data referenced by the file mapping.</span></span> <span data-ttu-id="1e464-133">Les données de paquets brutes suivent l' **\_ en-tête SHAREDMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="1e464-133">The raw packet data follows the **SHAREDMEMORY\_HEADER**.</span></span> <span data-ttu-id="1e464-134">Les données de paquets brutes peuvent être lues à partir de la mémoire partagée lorsque l’événement référencé par *pdwEventClientReadyId* est déclenché.</span><span class="sxs-lookup"><span data-stu-id="1e464-134">Raw packet data can be read off of the shared memory when the event referenced by *pdwEventClientReadyId* is raised.</span></span>

<span data-ttu-id="1e464-135">La liste suivante décrit la séquence d’événements pour l’accès à et l’utilisation de la mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1e464-135">The following list describes the sequence of events for accessing and using shared memory.</span></span>

1.  <span data-ttu-id="1e464-136">Le client déclenche l’événement clientReady.</span><span class="sxs-lookup"><span data-stu-id="1e464-136">The client raises the clientReady event.</span></span>
2.  <span data-ttu-id="1e464-137">Le client attend l’événement moreData.</span><span class="sxs-lookup"><span data-stu-id="1e464-137">The client waits for the moreData event.</span></span>
3.  <span data-ttu-id="1e464-138">Le client acquiert le mutex.</span><span class="sxs-lookup"><span data-stu-id="1e464-138">The client acquires the mutex.</span></span>
4.  <span data-ttu-id="1e464-139">Le client lit les données de paquets à partir de la section de la mémoire partagée qui suit l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="1e464-139">The client reads packet data from the section of shared memory that follows the header.</span></span> <span data-ttu-id="1e464-140">Les numéros de série s’affichent dans la mémoire partagée après les données du paquet.</span><span class="sxs-lookup"><span data-stu-id="1e464-140">Serial numbers appear in the shared memory after the packet data.</span></span>
5.  <span data-ttu-id="1e464-141">Le client gère les données en fonction de la valeur de **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="1e464-141">The client handles data depending on the value of **dwEvent**.</span></span>
6.  <span data-ttu-id="1e464-142">Le client écrit-1 (0xFFFFFFFF) dans **dwEvent**.</span><span class="sxs-lookup"><span data-stu-id="1e464-142">The client writes -1 (0xFFFFFFFF) into **dwEvent**.</span></span>
7.  <span data-ttu-id="1e464-143">Le client libère le mutex.</span><span class="sxs-lookup"><span data-stu-id="1e464-143">The client releases the mutex.</span></span>
8.  <span data-ttu-id="1e464-144">Le client déclenche l’événement clientReady.</span><span class="sxs-lookup"><span data-stu-id="1e464-144">The client raises the clientReady event.</span></span>

<span data-ttu-id="1e464-145">Les noms d’événements sont créés en mettant en forme la sortie de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1e464-145">The event names are created by formatting the output of this method.</span></span> <span data-ttu-id="1e464-146">Les définitions suivantes peuvent être utilisées conjointement avec sprintf ou son équivalent pour créer les noms d’événements.</span><span class="sxs-lookup"><span data-stu-id="1e464-146">The following definitions can be used in conjunction with sprintf or its equivalent to create the event names.</span></span>


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



<span data-ttu-id="1e464-147">Dans chaque définition, la section% d est remplacée par l’ID de processus, et la section% u est remplacée par l’entier retourné dans *pdwEventMoreDataId* ou *pdwEventClientReadyId*.</span><span class="sxs-lookup"><span data-stu-id="1e464-147">In each definition, the %d section is replaced with the process ID, and the %u section is replaced with the integer returned in *pdwEventMoreDataId* or *pdwEventClientReadyId*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e464-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e464-148">Requirements</span></span>



| <span data-ttu-id="1e464-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e464-149">Requirement</span></span> | <span data-ttu-id="1e464-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e464-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e464-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e464-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1e464-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e464-152">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e464-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e464-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1e464-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e464-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1e464-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e464-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e464-156"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e464-156"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e464-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e464-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e464-158">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="1e464-158">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[<span data-ttu-id="1e464-159">**ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="1e464-159">**ITabletContextP**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




