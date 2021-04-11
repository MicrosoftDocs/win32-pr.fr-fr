---
description: Actualise les informations d’interface pour une interface de réseau local sans fil spécifique.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: WZCRefreshInterface, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320221"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="328af-103">WZCRefreshInterface fonction)</span><span class="sxs-lookup"><span data-stu-id="328af-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="328af-104">\[**WZCRefreshInterface** n’est pas pris en charge à compter de Windows Vista et de windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="328af-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="328af-105">Utilisez plutôt l' [API WiFi Native](native-wifi-reference.md), qui offre des fonctionnalités similaires.</span><span class="sxs-lookup"><span data-stu-id="328af-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="328af-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="328af-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="328af-107">La fonction **WZCRefreshInterface** actualise les informations d’interface pour une interface de réseau local sans fil spécifique.</span><span class="sxs-lookup"><span data-stu-id="328af-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="328af-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="328af-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="328af-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="328af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="328af-110">*pSrvAddr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="328af-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="328af-111">Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="328af-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="328af-112">Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est appelé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="328af-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="328af-113">Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.</span><span class="sxs-lookup"><span data-stu-id="328af-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="328af-114">*dwInFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="328af-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="328af-115">Ensemble de champs à actualiser, ainsi que des actions d’actualisation spécifiques à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="328af-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="328af-116">Il s’agit d’un masque de masque qui peut contenir n’importe quelle combinaison des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="328af-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="328af-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="328af-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="328af-118">Signification</span><span class="sxs-lookup"><span data-stu-id="328af-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="328af-119"><dt>**INTF \_ DESCr**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="328af-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="328af-120">Actualisez la description de l’interface pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="328af-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="328af-121">La description de l’interface actualisée peut être récupérée en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) avec le bit **\_ descr INTF** défini dans le paramètre *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="328af-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="328af-122">La description de l’interface est retournée dans le membre **wszDescr** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* retourné par la fonction **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="328af-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="328af-123"><dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="328af-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="328af-124">Actualiser les informations de média NDIS pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="328af-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="328af-125">Les informations de média NDIS actualisées peuvent être récupérées en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) avec le bit **INTF \_ NDISMEDIA** défini dans le paramètre *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="328af-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="328af-126">Les informations de média NDIS sont retournées dans les membres **ulMediaState**, **ulMediaType** et **ulPhysicalMediaType** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* retourné par la fonction **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="328af-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="328af-127"><dt>**INTF \_ Tous les \_ OID**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="328af-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="328af-128">Actualiser tous les OID NDIS pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="328af-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="328af-129">Cette option actualise la plupart des données pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="328af-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="328af-130">Les informations actualisées peuvent être récupérées en appelant la fonction [**WZCQueryInterface**](wzcqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="328af-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="328af-131">*pIntf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="328af-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="328af-132">Pointeur vers une structure [**d' \_ entrée INTF**](intf-entry.md) qui contient la clé de l’interface à actualiser.</span><span class="sxs-lookup"><span data-stu-id="328af-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="328af-133">*pdwOutFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="328af-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="328af-134">Ensemble de champs qui ont été correctement actualisés.</span><span class="sxs-lookup"><span data-stu-id="328af-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="328af-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="328af-135">Return value</span></span>

<span data-ttu-id="328af-136">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="328af-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="328af-137">Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="328af-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="328af-138">Code de retour</span><span class="sxs-lookup"><span data-stu-id="328af-138">Return code</span></span>                                                                                              | <span data-ttu-id="328af-139">Description</span><span class="sxs-lookup"><span data-stu-id="328af-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="328af-140"><dt>**ERREUR de la \_ \_ Corbeille**</dt></span><span class="sxs-lookup"><span data-stu-id="328af-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="328af-141">Les blocs de contrôle de stockage ont été détruits.</span><span class="sxs-lookup"><span data-stu-id="328af-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="328af-142">Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.</span><span class="sxs-lookup"><span data-stu-id="328af-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="328af-143"><dt>**\_fichier d' \_ erreur \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="328af-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="328af-144">Le système ne peut pas trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="328af-144">The system cannot find the file specified.</span></span> <span data-ttu-id="328af-145">Cette erreur est retournée si le GUID dans le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* ne correspond à aucune des interfaces de réseau local sans fil sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="328af-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="328af-146"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="328af-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="328af-147">Un paramètre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="328af-147">A parameter is incorrect.</span></span> <span data-ttu-id="328af-148">Cette erreur est retournée si le paramètre *pIntf* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="328af-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="328af-149">Cette erreur est retournée si le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="328af-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="328af-150"><dt>**\_état RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="328af-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="328af-151">Divers codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="328af-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="328af-152">Notes</span><span class="sxs-lookup"><span data-stu-id="328af-152">Remarks</span></span>

<span data-ttu-id="328af-153">Le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* doit contenir un GUID d’interface pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="328af-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="328af-154">Une liste d’interfaces de réseau local sans fil peut être récupérée en appelant la fonction [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="328af-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="328af-155">Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="328af-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="328af-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="328af-156">Requirements</span></span>



| <span data-ttu-id="328af-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="328af-157">Requirement</span></span> | <span data-ttu-id="328af-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="328af-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="328af-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="328af-159">Minimum supported client</span></span><br/> | <span data-ttu-id="328af-160">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="328af-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="328af-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="328af-161">Minimum supported server</span></span><br/> | <span data-ttu-id="328af-162">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="328af-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="328af-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="328af-163">End of client support</span></span><br/>    | <span data-ttu-id="328af-164">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="328af-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="328af-165">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="328af-165">End of server support</span></span><br/>    | <span data-ttu-id="328af-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="328af-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="328af-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="328af-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="328af-168"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="328af-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="328af-169">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="328af-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="328af-170"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="328af-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="328af-171">DLL</span><span class="sxs-lookup"><span data-stu-id="328af-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="328af-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="328af-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328af-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="328af-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328af-174">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="328af-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="328af-175">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="328af-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="328af-176">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="328af-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="328af-177">**\_entrée INTF**</span><span class="sxs-lookup"><span data-stu-id="328af-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




