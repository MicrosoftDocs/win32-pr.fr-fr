---
description: Fournit des informations détaillées pour une interface de réseau local sans fil gérée par le service de configuration sans fil de zéro.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: WZCQueryInterface, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867902"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="c822a-103">WZCQueryInterface fonction)</span><span class="sxs-lookup"><span data-stu-id="c822a-103">WZCQueryInterface function</span></span>

<span data-ttu-id="c822a-104">\[**WZCQueryInterface** n’est plus pris en charge à compter de Windows Vista et de windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c822a-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c822a-105">Utilisez à la place la fonction [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="c822a-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="c822a-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="c822a-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="c822a-107">\]</span><span class="sxs-lookup"><span data-stu-id="c822a-107">\]</span></span>

<span data-ttu-id="c822a-108">La fonction **WZCQueryInterface** fournit des informations détaillées pour une interface de réseau local sans fil gérée par le service de configuration sans fil Zero.</span><span class="sxs-lookup"><span data-stu-id="c822a-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="c822a-109">Fournit des informations détaillées sur une interface donnée.</span><span class="sxs-lookup"><span data-stu-id="c822a-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c822a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c822a-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c822a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c822a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c822a-112">*pSrvAddr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c822a-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c822a-113">Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="c822a-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="c822a-114">Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est interrogé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c822a-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="c822a-115">Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.</span><span class="sxs-lookup"><span data-stu-id="c822a-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="c822a-116">*dwInFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c822a-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c822a-117">Champs à interroger.</span><span class="sxs-lookup"><span data-stu-id="c822a-117">The fields to be queried.</span></span> <span data-ttu-id="c822a-118">Il s’agit d’un masque de masque qui peut contenir n’importe quelle combinaison des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="c822a-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="c822a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c822a-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="c822a-120">Signification</span><span class="sxs-lookup"><span data-stu-id="c822a-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="c822a-121"><dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="c822a-122">Retournez la valeur du membre **dwDynFlags** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="c822a-123"><dt>**INTF \_ DESCr**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="c822a-124">Retournez la valeur du membre **wszDescr** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="c822a-125"><dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="c822a-126">Retournez les valeurs pour les membres **ulMediaState**, **ulMediaType** et **ulPhysicalMediaType** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="c822a-127"><dt>**INTF \_ PREFLIST**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="c822a-128">Retourne la liste par défaut des réseaux dans le membre **rdStSSIDList** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="c822a-129"><dt>**INTF \_ FONCTIONNALITÉS**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="c822a-130">Retournez les valeurs pour les membres **dwCapabilities** et **rdNicCapabilities** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="c822a-131"><dt>**INTF \_ INFRAMODE**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="c822a-132">Retournez la valeur du membre **nInfraMode** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="c822a-133">Le membre **nInfraMode** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="c822a-134"><dt>**INTF \_ AUTHMODE**</dt> <dt>0x00400000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="c822a-135">Retournez la valeur du membre **nAuthMode** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="c822a-136">Le membre **nAuthMode** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="c822a-137"><dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="c822a-138">Retournez la valeur du membre **nWepStatus** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="c822a-139">Le membre **nWepStatus** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="c822a-140"><dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="c822a-141">Retournez la valeur du membre **rdSSID** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="c822a-142">Le membre **rdSSID** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="c822a-143"><dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="c822a-144">Retournez la valeur du membre **rdBSSID** dans la structure [**d' \_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="c822a-145">Le membre **rdBSSID** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="c822a-146"><dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="c822a-147">Retourne la liste visible des réseaux dans le membre **rdBSSIDList** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="c822a-148">Le membre **rdBSSIDList** est valide uniquement dans certains États de contexte d’interface.</span><span class="sxs-lookup"><span data-stu-id="c822a-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c822a-149">*pIntf* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c822a-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c822a-150">En entrée, pointeur vers la clé de l’interface à interroger.</span><span class="sxs-lookup"><span data-stu-id="c822a-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="c822a-151">Lors de la sortie, pointeur vers les données d’interface demandées.</span><span class="sxs-lookup"><span data-stu-id="c822a-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="c822a-152">Ce paramètre est un pointeur vers une structure d' [**\_ entrée INTF**](intf-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="c822a-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c822a-153">*pdwOutFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c822a-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c822a-154">Un ensemble de champs correctement récupérés.</span><span class="sxs-lookup"><span data-stu-id="c822a-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c822a-155">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c822a-155">Return value</span></span>

<span data-ttu-id="c822a-156">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="c822a-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c822a-157">Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c822a-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="c822a-158">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c822a-158">Return code</span></span>                                                                                               | <span data-ttu-id="c822a-159">Description</span><span class="sxs-lookup"><span data-stu-id="c822a-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c822a-160"><dt>**ERREUR de la \_ \_ Corbeille**</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="c822a-161">Les blocs de contrôle de stockage ont été détruits.</span><span class="sxs-lookup"><span data-stu-id="c822a-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="c822a-162">Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.</span><span class="sxs-lookup"><span data-stu-id="c822a-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="c822a-163"><dt>**\_fichier d' \_ erreur \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="c822a-164">Le système ne peut pas trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c822a-164">The system cannot find the file specified.</span></span> <span data-ttu-id="c822a-165">Cette erreur est retournée si le GUID dans le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* ne correspond à aucune des interfaces de réseau local sans fil sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c822a-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="c822a-166"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="c822a-167">Un paramètre est incorrect.</span><span class="sxs-lookup"><span data-stu-id="c822a-167">A parameter is incorrect.</span></span> <span data-ttu-id="c822a-168">Cette erreur est retournée si le paramètre *pIntf* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c822a-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="c822a-169">Cette erreur est retournée si le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c822a-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="c822a-170"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="c822a-171">Mémoire disponible insuffisante pour traiter cette demande et allouer de la mémoire pour les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="c822a-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="c822a-172"><dt>**\_état RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="c822a-173">Divers codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c822a-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="c822a-174">Notes</span><span class="sxs-lookup"><span data-stu-id="c822a-174">Remarks</span></span>

<span data-ttu-id="c822a-175">Le membre **wszGuid** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* doit contenir un GUID d’interface pour une interface de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="c822a-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="c822a-176">Une liste d’interfaces de réseau local sans fil peut être récupérée en appelant la fonction [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="c822a-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="c822a-177">Les membres suivants de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe *pIntf* doit avoir la valeur 0 avant un appel à la fonction **WZCQueryInterface** : **RdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** et **rdCtrlData**.</span><span class="sxs-lookup"><span data-stu-id="c822a-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="c822a-178">Le service de configuration sans fil Zero automotically ne met pas à jour l’état du support, même lorsque des événements Media Connected et Disconnected sont reçus.</span><span class="sxs-lookup"><span data-stu-id="c822a-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="c822a-179">Une application doit forcer l’actualisation de l’état d’un média en appelant la fonction [**WZCRefreshInterface**](wzcrefreshinterface.md) avant d’appeler la fonction **WZCQueryInterface** si l’état du média NDIS doit être demandé (le \_ bit INTF NDISMEDIA est défini dans le paramètre *dwInFlags* ).</span><span class="sxs-lookup"><span data-stu-id="c822a-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="c822a-180">Lorsque le paramètre *dwInFlags* contient **INTF \_ BSSIDLIST**, la fonction **WZCQueryInterface** ne définit pas l' *dwOutFlags* avec **INTF \_ BSSIDLIST** si la liste visible des réseaux est vide.</span><span class="sxs-lookup"><span data-stu-id="c822a-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="c822a-181">Lorsque le paramètre *dwInFlags* contient **INTF \_ SSID**, la fonction **WZCQueryInterface** ne définit pas le *dwOutFlags* avec **INTF \_ SSID** si aucun SSID n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="c822a-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="c822a-182">Si la fonction **WZCQueryInterface** retourne \_ une erreur, l’appelant doit appeler la fonction [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) avec le paramètre *pIntf* pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="c822a-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="c822a-183">Cela libère les mémoires tampons utilisées par les membres **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList** et **rdCtrlData** de la structure d' [**\_ entrée INTF**](intf-entry.md) vers laquelle pointe le paramètre *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="c822a-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="c822a-184">Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c822a-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c822a-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c822a-185">Requirements</span></span>



| <span data-ttu-id="c822a-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c822a-186">Requirement</span></span> | <span data-ttu-id="c822a-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="c822a-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c822a-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c822a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="c822a-189">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c822a-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c822a-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c822a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="c822a-191">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c822a-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c822a-192">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c822a-192">End of client support</span></span><br/>    | <span data-ttu-id="c822a-193">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="c822a-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="c822a-194">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c822a-194">End of server support</span></span><br/>    | <span data-ttu-id="c822a-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c822a-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c822a-196">En-tête</span><span class="sxs-lookup"><span data-stu-id="c822a-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="c822a-197"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c822a-198">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c822a-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="c822a-199"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c822a-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c822a-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c822a-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c822a-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c822a-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c822a-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c822a-203">**\_entrée INTF**</span><span class="sxs-lookup"><span data-stu-id="c822a-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="c822a-204">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="c822a-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="c822a-205">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="c822a-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="c822a-206">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="c822a-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
