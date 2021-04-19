---
title: RasAdminPortClearStatistics, fonction (rassapi. h)
description: La fonction RasAdminPortClearStatistics réinitialise les compteurs représentant les diverses statistiques signalées par la fonction RasAdminPortGetInfo dans la structure des \_ statistiques du port RAS \_ . Les compteurs sont remis à zéro et commencent à s’accumuler.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532625"
---
# <a name="rasadminportclearstatistics-function"></a><span data-ttu-id="56196-105">RasAdminPortClearStatistics fonction)</span><span class="sxs-lookup"><span data-stu-id="56196-105">RasAdminPortClearStatistics function</span></span>

<span data-ttu-id="56196-106">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="56196-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="56196-107">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="56196-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="56196-108">Les applications doivent utiliser la fonction [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]</span><span class="sxs-lookup"><span data-stu-id="56196-108">Applications should use the [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) function.\]</span></span>

<span data-ttu-id="56196-109">La fonction **RasAdminPortClearStatistics** réinitialise les compteurs représentant les diverses statistiques signalées par la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) dans la structure [**des \_ \_ statistiques du port RAS**](ras-port-statistics-str.md) .</span><span class="sxs-lookup"><span data-stu-id="56196-109">The **RasAdminPortClearStatistics** function resets the counters representing the various statistics reported by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function in the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure.</span></span> <span data-ttu-id="56196-110">Les compteurs sont remis à zéro et commencent à s’accumuler.</span><span class="sxs-lookup"><span data-stu-id="56196-110">The counters are reset to zero and start accumulating.</span></span>

## <a name="syntax"></a><span data-ttu-id="56196-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56196-111">Syntax</span></span>


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="56196-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56196-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56196-113">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56196-113">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56196-114">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="56196-114">Pointer to a null-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="56196-115">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="56196-115">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="56196-116">*lpszPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56196-116">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56196-117">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="56196-117">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56196-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56196-118">Return value</span></span>

<span data-ttu-id="56196-119">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="56196-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="56196-120">Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="56196-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="56196-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56196-121">Value</span></span>                                                                                                 | <span data-ttu-id="56196-122">Signification</span><span class="sxs-lookup"><span data-stu-id="56196-122">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="56196-123"><dt>**ERREUR \_ de \_ développement \_ inexistant**</dt></span><span class="sxs-lookup"><span data-stu-id="56196-123"><dt>**ERROR\_DEV\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="56196-124">Le port spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="56196-124">The specified port is invalid.</span></span><br/> |



 

<span data-ttu-id="56196-125">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="56196-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="56196-126">Notes</span><span class="sxs-lookup"><span data-stu-id="56196-126">Remarks</span></span>

<span data-ttu-id="56196-127">La fonction **RasAdminPortClearStatistics** efface les statistiques sur le serveur, pas localement au sein de l’application qui effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="56196-127">The **RasAdminPortClearStatistics** function clears the statistics on the server, not locally within the application that makes the call.</span></span> <span data-ttu-id="56196-128">Cela signifie que les statistiques sont également réinitialisées pour toute autre application qui surveille le port spécifié.</span><span class="sxs-lookup"><span data-stu-id="56196-128">This means that the statistics are also reset for any other application that is monitoring the specified port.</span></span>

<span data-ttu-id="56196-129">Si le port *lpszPort* fait partie d’une connexion multilien, **RasAdminPortClearStatistics** réinitialise les statistiques pour le port spécifié, la fonction réinitialise également les statistiques cumulatives pour la connexion à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="56196-129">If the *lpszPort* port is part of a multilink connection, **RasAdminPortClearStatistics** resets the statistics for the specified port, The function also resets the cumulative statistics for the multilink connection.</span></span> <span data-ttu-id="56196-130">Toutefois, la fonction n’affecte pas les statistiques individuelles pour les autres ports qui font partie de la connexion à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="56196-130">However, the function does not effect the individual statistics for other ports that are part of the multilink connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="56196-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56196-131">Requirements</span></span>



| <span data-ttu-id="56196-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56196-132">Requirement</span></span> | <span data-ttu-id="56196-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="56196-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56196-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="56196-134">End of client support</span></span><br/> | <span data-ttu-id="56196-135">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="56196-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="56196-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="56196-136">End of server support</span></span><br/> | <span data-ttu-id="56196-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56196-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="56196-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="56196-138">Header</span></span><br/>                | <dl> <span data-ttu-id="56196-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56196-139"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="56196-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56196-140">Library</span></span><br/>               | <dl> <span data-ttu-id="56196-141"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56196-141"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="56196-142">DLL</span><span class="sxs-lookup"><span data-stu-id="56196-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="56196-143"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56196-143"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56196-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56196-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56196-145">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="56196-145">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="56196-146">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="56196-146">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="56196-147">**\_statistiques du port RAS \_**</span><span class="sxs-lookup"><span data-stu-id="56196-147">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="56196-148">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="56196-148">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

