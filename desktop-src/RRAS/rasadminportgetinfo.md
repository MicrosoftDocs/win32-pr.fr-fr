---
title: RasAdminPortGetInfo, fonction (rassapi. h)
description: La fonction RasAdminPortGetInfo récupère des informations sur un port spécifié sur un serveur spécifié.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522822"
---
# <a name="rasadminportgetinfo-function"></a><span data-ttu-id="101f1-104">RasAdminPortGetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="101f1-104">RasAdminPortGetInfo function</span></span>

<span data-ttu-id="101f1-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="101f1-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="101f1-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="101f1-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="101f1-107">Les applications doivent utiliser la fonction [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="101f1-107">Applications should use the [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) function.\]</span></span>

<span data-ttu-id="101f1-108">La fonction **RasAdminPortGetInfo** récupère des informations sur un port spécifié sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="101f1-108">The **RasAdminPortGetInfo** function retrieves information about a specified port on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="101f1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="101f1-109">Syntax</span></span>


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
);
```



## <a name="parameters"></a><span data-ttu-id="101f1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="101f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101f1-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="101f1-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101f1-112">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="101f1-112">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="101f1-113">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="101f1-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="101f1-114">*lpszPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="101f1-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101f1-115">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="101f1-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> <dt>

<span data-ttu-id="101f1-116">*pRasPort1* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="101f1-116">*pRasPort1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101f1-117">Pointeur vers la structure du [**\_ port \_ 1 RAS**](ras-port-1-str.md) que la fonction remplit à l’aide d’informations sur l’état du port.</span><span class="sxs-lookup"><span data-stu-id="101f1-117">Pointer to the [**RAS\_PORT\_1**](ras-port-1-str.md) structure that the function fills in with information about the state of the port.</span></span>

</dd> <dt>

<span data-ttu-id="101f1-118">*pRasStats* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="101f1-118">*pRasStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101f1-119">Pointeur vers la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) que la fonction remplit avec des statistiques sur le port.</span><span class="sxs-lookup"><span data-stu-id="101f1-119">Pointer to the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure that the function fills in with statistics about the port.</span></span>

</dd> <dt>

<span data-ttu-id="101f1-120">*ppRasParams* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="101f1-120">*ppRasParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101f1-121">Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) .</span><span class="sxs-lookup"><span data-stu-id="101f1-121">Pointer to a pointer variable that receives the address of an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures.</span></span> <span data-ttu-id="101f1-122">Chaque structure contient le nom d’une clé spécifique au support, par exemple MAXCONNECTBPS, et sa valeur associée.</span><span class="sxs-lookup"><span data-stu-id="101f1-122">Each structure contains the name of a media-specific key, such as MAXCONNECTBPS, and its associated value.</span></span> <span data-ttu-id="101f1-123">Lorsque l’application a terminé cette mémoire, libérez-la en appelant la fonction [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="101f1-123">When the application is finished with this memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101f1-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="101f1-124">Return value</span></span>

<span data-ttu-id="101f1-125">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="101f1-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="101f1-126">Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="101f1-126">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="101f1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="101f1-127">Value</span></span>                                                                                                     | <span data-ttu-id="101f1-128">Signification</span><span class="sxs-lookup"><span data-stu-id="101f1-128">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="101f1-129"><dt>**ERREUR \_ de \_ développement \_ inexistant**</dt></span><span class="sxs-lookup"><span data-stu-id="101f1-129"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl>     | <span data-ttu-id="101f1-130">Le port spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="101f1-130">The specified port is invalid.</span></span><br/>                                        |
| <dl> <span data-ttu-id="101f1-131"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="101f1-131"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="101f1-132">Mémoire insuffisante pour allouer une mémoire tampon pour le tableau *ppRasParams* .</span><span class="sxs-lookup"><span data-stu-id="101f1-132">Insufficient memory to allocate a buffer for the *ppRasParams* array.</span></span><br/> |



 

<span data-ttu-id="101f1-133">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="101f1-133">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="101f1-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="101f1-134">Requirements</span></span>



| <span data-ttu-id="101f1-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="101f1-135">Requirement</span></span> | <span data-ttu-id="101f1-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="101f1-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="101f1-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="101f1-137">End of client support</span></span><br/> | <span data-ttu-id="101f1-138">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="101f1-138">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="101f1-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="101f1-139">End of server support</span></span><br/> | <span data-ttu-id="101f1-140">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="101f1-140">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="101f1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="101f1-141">Header</span></span><br/>                | <dl> <span data-ttu-id="101f1-142"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="101f1-142"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="101f1-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="101f1-143">Library</span></span><br/>               | <dl> <span data-ttu-id="101f1-144"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="101f1-144"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="101f1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="101f1-145">DLL</span></span><br/>                   | <dl> <span data-ttu-id="101f1-146"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="101f1-146"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="101f1-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="101f1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101f1-148">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="101f1-148">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="101f1-149">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="101f1-149">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="101f1-150">**\_paramètres RAS**</span><span class="sxs-lookup"><span data-stu-id="101f1-150">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="101f1-151">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="101f1-151">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="101f1-152">**\_statistiques du port RAS \_**</span><span class="sxs-lookup"><span data-stu-id="101f1-152">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="101f1-153">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="101f1-153">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

