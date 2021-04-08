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
# <a name="wzcenuminterfaces-function"></a>WZCEnumInterfaces fonction)

\[**WZCEnumInterfaces** n’est plus pris en charge à compter de Windows Vista et de windows Server 2008. Utilisez plutôt la fonction [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) . Pour plus d’informations, consultez [à propos de l’API WiFi Native](about-the-native-wifi-api.md).\]

La fonction **WZCEnumInterfaces** énumère toutes les interfaces de réseau local sans fil gérées par le service de configuration sans fil Zero.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrvAddr* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne contenant le nom de l’ordinateur sur lequel exécuter cette fonction. Si ce paramètre a la **valeur null**, le service de configuration sans fil Zero est énuméré sur l’ordinateur local.

Si le paramètre *pSrvAddr* spécifié est un ordinateur distant, l’ordinateur distant doit prendre en charge les appels RPC distants.

</dd> <dt>

*pIntfs* \[ à\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ table de clé INTFS**](intfs-key-table.md) qui contient une table d’informations de clé pour toutes les interfaces.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.



| Code de retour                                                                                               | Description                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de la \_ \_ Corbeille**</dt> </dl>      | Les blocs de contrôle de stockage ont été détruits. Cette erreur est retournée si le service de configuration sans fil Zero n’a pas initialisé d’objets internes.<br/> |
| <dl> <dt>**RPC \_ S \_ inconnu \_ si**</dt> </dl>        | L’interface est inconnue.<br/> Cette erreur est retournée si le service de configuration sans fil Zero n’est pas démarré.<br/>                             |
| <dl> <dt>**\_ \_ \_ pointeur Ref null RPC \_ X**</dt> </dl> | Un pointeur de référence null a été passé au stub.<br/> Cette erreur est retournée si le paramètre *pIntfs* a la **valeur null**.<br/>                          |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl> | Mémoire disponible insuffisante pour traiter cette demande et allouer de la mémoire pour les résultats de la requête.<br/>                                                  |
| <dl> <dt>**\_état RPC**</dt> </dl>                | Divers codes d’erreur.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Notes

Le membre **dwNumIntfs** de la structure de [**\_ \_ table de clé INTFS**](intfs-key-table.md) vers laquelle pointe *pIntf* doit avoir la valeur 0 avant d’appeler la fonction **WZCEnumInterfaces** . En outre, le membre **pIntfs** doit avoir la valeur **null**.

Pour les appels suivants à d’autres fonctions de configuration sans fil sans fil, une application doit identifier l’interface sur laquelle elle fonctionne en fournissant les informations de clé pertinentes retournées par la fonction **WZCEnumInterfaces** .

Si le **WZCEnumInterfaces** retourne \_ une erreur, l’appelant doit appeler [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) pour libérer les mémoires tampons internes allouées pour les données retournées une fois que ces informations ne sont plus nécessaires.

> [!Note]  
> Le fichier d’en-tête *wzcsapi. h* et le fichier de bibliothèque d’importation *wzcsapi. lib* ne sont pas disponibles dans le SDK Windows.

 

## <a name="examples"></a>Exemples

L’exemple suivant énumère les interfaces de réseau local sans fil sur l’ordinateur local géré par le service de configuration sans fil Zero et imprime la valeur du GUID d’interface pour chaque interface.

> [!Note]  
> Cet exemple échoue sur Windows Vista et versions ultérieures.

 


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| Fin de la prise en charge des clients<br/>    | Windows XP avec SP3<br/>                                                         |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_table de clé INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**\_entrée de clé INTF \_**](intf-key-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
