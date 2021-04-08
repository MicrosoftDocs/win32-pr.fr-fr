---
description: Énumère toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil Zero.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: WZCEnumInterfaces, fonction (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867901"
---
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="d8b66-103">WZCEnumInterfaces fonction)</span><span class="sxs-lookup"><span data-stu-id="d8b66-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="d8b66-104">\[**WZCEnumInterfaces** n’est plus pris en charge à compter de Windows Vista et de windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d8b66-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="d8b66-105">Utilisez plutôt la fonction [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) .</span><span class="sxs-lookup"><span data-stu-id="d8b66-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="d8b66-106">Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="d8b66-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="d8b66-107">La fonction **WZCEnumInterfaces** énumère toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil Zero.</span><span class="sxs-lookup"><span data-stu-id="d8b66-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b66-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8b66-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="d8b66-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8b66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b66-110">*pSrvAddr* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8b66-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b66-111">Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="d8b66-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="d8b66-112">Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est énuméré sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d8b66-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="d8b66-113">Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.</span><span class="sxs-lookup"><span data-stu-id="d8b66-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="d8b66-114">*pIntfs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8b66-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b66-115">Pointeur vers une structure [**de \_ \_ table de clé INTFS**](intfs-key-table.md) qui contient une table d’informations de clé pour toutes les interfaces.</span><span class="sxs-lookup"><span data-stu-id="d8b66-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b66-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8b66-116">Return value</span></span>

<span data-ttu-id="d8b66-117">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="d8b66-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d8b66-118">Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="d8b66-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="d8b66-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d8b66-119">Return code</span></span>                                                                                               | <span data-ttu-id="d8b66-120">Description</span><span class="sxs-lookup"><span data-stu-id="d8b66-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8b66-121"><dt>**ERREUR de la \_ \_ Corbeille**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="d8b66-122">Les blocs de contrôle de stockage ont été détruits.</span><span class="sxs-lookup"><span data-stu-id="d8b66-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="d8b66-123">Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.</span><span class="sxs-lookup"><span data-stu-id="d8b66-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="d8b66-124"><dt>**RPC \_ S \_ inconnu \_ si**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="d8b66-125">L’interface est inconnue.</span><span class="sxs-lookup"><span data-stu-id="d8b66-125">The interface is unknown.</span></span><br/> <span data-ttu-id="d8b66-126">Cette erreur est retournée si le service de configuration sans fil Zero n’est pas démarré.</span><span class="sxs-lookup"><span data-stu-id="d8b66-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="d8b66-127"><dt>**\_ \_ \_ pointeur Ref null RPC \_ X**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d8b66-128">Un pointeur de référence null a été passé au stub.</span><span class="sxs-lookup"><span data-stu-id="d8b66-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="d8b66-129">Cette erreur est retournée si le paramètre *pIntfs* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d8b66-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="d8b66-130"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="d8b66-131">Mémoire disponible insuffisante pour traiter cette demande et allouer de la mémoire pour les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="d8b66-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="d8b66-132"><dt>**\_état RPC**</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="d8b66-133">Divers codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8b66-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d8b66-134">Notes</span><span class="sxs-lookup"><span data-stu-id="d8b66-134">Remarks</span></span>

<span data-ttu-id="d8b66-135">Le membre **dwNumIntfs** de la structure de [**\_ \_ table de clé INTFS**](intfs-key-table.md) vers laquelle pointe *pIntf* doit avoir la valeur 0 avant d’appeler la fonction **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="d8b66-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="d8b66-136">En outre, le membre **pIntfs** doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d8b66-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="d8b66-137">Pour les appels suivants à d’autres fonctions de configuration sans fil sans fil, une application doit identifier l’interface sur laquelle elle fonctionne en fournissant les informations de clé pertinentes retournées par la fonction **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="d8b66-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="d8b66-138">Si le **WZCEnumInterfaces** retourne \_ une erreur, l’appelant doit appeler [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d8b66-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="d8b66-139">Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d8b66-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d8b66-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="d8b66-140">Examples</span></span>

<span data-ttu-id="d8b66-141">L’exemple suivant énumère les interfaces de réseau local sans fil sur l’ordinateur local géré par le service de configuration sans fil Zero et imprime la valeur du GUID d’interface pour chaque interface.</span><span class="sxs-lookup"><span data-stu-id="d8b66-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="d8b66-142">Cet exemple échoue sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d8b66-142">This example will fail on Windows Vista and later .</span></span>

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="d8b66-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8b66-143">Requirements</span></span>



| <span data-ttu-id="d8b66-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8b66-144">Requirement</span></span> | <span data-ttu-id="d8b66-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8b66-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b66-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b66-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b66-147">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8b66-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d8b66-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8b66-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b66-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8b66-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d8b66-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d8b66-150">End of client support</span></span><br/>    | <span data-ttu-id="d8b66-151">Windows XP avec SP3</span><span class="sxs-lookup"><span data-stu-id="d8b66-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="d8b66-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d8b66-152">End of server support</span></span><br/>    | <span data-ttu-id="d8b66-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8b66-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d8b66-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8b66-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b66-155"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8b66-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8b66-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8b66-157"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d8b66-158">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b66-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b66-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8b66-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b66-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8b66-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b66-161">**\_table de clé INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="d8b66-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="d8b66-162">**\_entrée de clé INTF \_**</span><span class="sxs-lookup"><span data-stu-id="d8b66-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="d8b66-163">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="d8b66-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="d8b66-164">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="d8b66-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="d8b66-165">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="d8b66-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
