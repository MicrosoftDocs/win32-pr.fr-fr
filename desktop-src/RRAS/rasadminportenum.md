---
title: RasAdminPortEnum, fonction (rassapi. h)
description: La fonction RasAdminPortEnum énumère tous les ports sur le serveur RAS spécifié. Pour chaque port sur le serveur, la fonction retourne la \_ structure du port RAS \_ 0 qui contient des informations sur le port.
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e4841627ce5df3feee3f885b399a070388ed55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533058"
---
# <a name="rasadminportenum-function"></a><span data-ttu-id="05386-105">RasAdminPortEnum fonction)</span><span class="sxs-lookup"><span data-stu-id="05386-105">RasAdminPortEnum function</span></span>

<span data-ttu-id="05386-106">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="05386-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="05386-107">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05386-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="05386-108">Les applications doivent utiliser la fonction [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) .\]</span><span class="sxs-lookup"><span data-stu-id="05386-108">Applications should use the [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) function.\]</span></span>

<span data-ttu-id="05386-109">La fonction **RasAdminPortEnum** énumère tous les ports sur le serveur RAS spécifié.</span><span class="sxs-lookup"><span data-stu-id="05386-109">The **RasAdminPortEnum** function enumerates all ports on the specified RAS server.</span></span> <span data-ttu-id="05386-110">Pour chaque port sur le serveur, la fonction retourne la structure du [**\_ port RAS \_ 0**](ras-port-0-str.md) qui contient des informations sur le port.</span><span class="sxs-lookup"><span data-stu-id="05386-110">For each port on the server, the function returns the [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port.</span></span>

## <a name="syntax"></a><span data-ttu-id="05386-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05386-111">Syntax</span></span>


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a><span data-ttu-id="05386-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05386-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05386-113">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05386-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05386-114">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="05386-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="05386-115">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="05386-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="05386-116">*ppRasPort0* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05386-116">*ppRasPort0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05386-117">Pointeur vers une variable qui reçoit un pointeur vers une mémoire tampon qui contient un tableau de structures du [**\_ port RAS \_ 0**](ras-port-0-str.md) .</span><span class="sxs-lookup"><span data-stu-id="05386-117">Pointer to a variable that receives a pointer to a buffer that contains an array of [**RAS\_PORT\_0**](ras-port-0-str.md) structures.</span></span> <span data-ttu-id="05386-118">Lorsque l’application a terminé la mémoire, libérez-la en appelant la fonction [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="05386-118">When the application has finished with the memory, free it by calling the [**RasAdminFreeBuffer**](rasadminfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="05386-119">*pcEntriesRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05386-119">*pcEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05386-120">Pointeur vers une variable de 16 bits qui reçoit le nombre total de structures [**RAS \_ port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) retournées dans le tableau *ppRasPort0* .</span><span class="sxs-lookup"><span data-stu-id="05386-120">Pointer to a 16-bit variable that receives the total number of [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) structures returned in the *ppRasPort0* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05386-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05386-121">Return value</span></span>

<span data-ttu-id="05386-122">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="05386-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="05386-123">Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="05386-123">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="05386-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="05386-124">Value</span></span>                                                                                             | <span data-ttu-id="05386-125">Signification</span><span class="sxs-lookup"><span data-stu-id="05386-125">Meaning</span></span>                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05386-126"><dt>**NERR \_ ItemNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="05386-126"><dt>**NERR\_ItemNotFound**</dt></span></span> </dl> | <span data-ttu-id="05386-127">Aucun port ne peut être énuméré.</span><span class="sxs-lookup"><span data-stu-id="05386-127">No ports could be enumerated.</span></span> <span data-ttu-id="05386-128">Cela peut être dû au fait que tous les ports configurés sur le serveur sont actuellement utilisés pour la numérotation.</span><span class="sxs-lookup"><span data-stu-id="05386-128">This could be because all configured ports on the server are currently being used for dialing out.</span></span><br/> |



 

<span data-ttu-id="05386-129">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="05386-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="05386-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05386-130">Requirements</span></span>



| <span data-ttu-id="05386-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05386-131">Requirement</span></span> | <span data-ttu-id="05386-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="05386-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05386-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="05386-133">End of client support</span></span><br/> | <span data-ttu-id="05386-134">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="05386-134">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="05386-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="05386-135">End of server support</span></span><br/> | <span data-ttu-id="05386-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05386-136">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="05386-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="05386-137">Header</span></span><br/>                | <dl> <span data-ttu-id="05386-138"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="05386-138"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="05386-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05386-139">Library</span></span><br/>               | <dl> <span data-ttu-id="05386-140"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05386-140"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="05386-141">DLL</span><span class="sxs-lookup"><span data-stu-id="05386-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="05386-142"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05386-142"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05386-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05386-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05386-144">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="05386-144">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="05386-145">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="05386-145">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="05386-146">**\_Port RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="05386-146">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="05386-147">**RasAdminFreeBuffer**</span><span class="sxs-lookup"><span data-stu-id="05386-147">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)
</dt> </dl>

 

