---
description: Obtient les paramètres de configuration EAPOL pour l’interface de réseau local sans fil spécifiée.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: WZCEapolGetInterfaceParams, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521924"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="77c76-103">WZCEapolGetInterfaceParams fonction)</span><span class="sxs-lookup"><span data-stu-id="77c76-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="77c76-104">\[**WZCEapolGetInterfaceParams** n’est plus pris en charge à compter de Windows Vista et de windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="77c76-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="77c76-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="77c76-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="77c76-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="77c76-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="77c76-107">La fonction **WZCEapolGetInterfaceParams** obtient les paramètres de configuration EAPOL pour l’interface de réseau local sans fil spécifiée.</span><span class="sxs-lookup"><span data-stu-id="77c76-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c76-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77c76-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="77c76-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77c76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77c76-110">*pSrvAddr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77c76-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c76-111">Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="77c76-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="77c76-112">Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est appelé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="77c76-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="77c76-113">Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.</span><span class="sxs-lookup"><span data-stu-id="77c76-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="77c76-114">*pwszGuid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77c76-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c76-115">GUID de l’interface pour laquelle les données doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="77c76-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="77c76-116">*dwSizeOfSSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77c76-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c76-117">Taille de l’identificateur réseau pour lequel les données doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="77c76-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="77c76-118">*pbSSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77c76-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77c76-119">Pointeur vers l’identificateur réseau pour lequel les données doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="77c76-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="77c76-120">*pIntfParams* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="77c76-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77c76-121">Pointeur vers une structure [**EAPOL \_ INTF \_ params**](eapol-intf-params.md) qui contient des paramètres d’interface.</span><span class="sxs-lookup"><span data-stu-id="77c76-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77c76-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77c76-122">Return value</span></span>

<span data-ttu-id="77c76-123">Retourne l’erreur \_ de réussite si l’opération se termine correctement ; sinon, retourne l’un des codes d’erreur système Windows.</span><span class="sxs-lookup"><span data-stu-id="77c76-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="77c76-124">Notes</span><span class="sxs-lookup"><span data-stu-id="77c76-124">Remarks</span></span>

<span data-ttu-id="77c76-125">Si le **WZCEapolGetInterfaceParams** retourne \_ une erreur, l’appelant doit appeler [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="77c76-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="77c76-126">Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="77c76-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77c76-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77c76-127">Requirements</span></span>



| <span data-ttu-id="77c76-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77c76-128">Requirement</span></span> | <span data-ttu-id="77c76-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="77c76-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77c76-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77c76-130">Minimum supported client</span></span><br/> | <span data-ttu-id="77c76-131">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77c76-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77c76-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77c76-132">Minimum supported server</span></span><br/> | <span data-ttu-id="77c76-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77c76-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77c76-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="77c76-134">End of client support</span></span><br/>    | <span data-ttu-id="77c76-135">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="77c76-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="77c76-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="77c76-136">End of server support</span></span><br/>    | <span data-ttu-id="77c76-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77c76-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="77c76-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="77c76-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="77c76-139"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77c76-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="77c76-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77c76-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="77c76-141"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77c76-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="77c76-142">DLL</span><span class="sxs-lookup"><span data-stu-id="77c76-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77c76-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77c76-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77c76-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77c76-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c76-145">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="77c76-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="77c76-146">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="77c76-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="77c76-147">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="77c76-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
