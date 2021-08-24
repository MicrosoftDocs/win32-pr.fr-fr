---
description: Les API de protection contre la perte de données (DLP) du point de terminaison permettent aux applications de notifier le système d’exploitation avant et après certaines opérations, telles que l’ouverture ou l’enregistrement d’un fichier.
title: Protection contre la perte de données de point de terminaison
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: fcbe17d30addb86e37330b210d224720f9b50e525e2b8d41d07d349ea5819c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479430"
---
# <a name="endpoint-data-loss-prevention"></a>Protection contre la perte de données de point de terminaison

Windows 10 implémente des mécanismes qui permettent d’éviter la perte de données pour les fichiers sensibles. Les API de protection contre la perte de données (DLP) du point de terminaison permettent aux applications de notifier le système d’exploitation avant et après certaines opérations, telles que l’ouverture ou l’enregistrement d’un fichier. Ces notifications servent d’indicateurs qui permettent au système d’optimiser les opérations de perte de données.

## <a name="location-of-the-dlp-dll"></a>Emplacement de la dll DLP

étant donné que la dll DLP du point de terminaison n’est pas regroupée avec le SDK Windows, les applications doivent charger la dll manuellement au moment de l’exécution. Le chemin d’accès à l’emplacement de la dll est stocké dans le registre. Le tableau suivant répertorie les clés de Registre et les valeurs qui stockent ces informations. Ces chemins d’accès sont définis en tant que constantes dans l’exemple de code endpointdlp. h fourni ci-dessous pour les développeurs.

| Constante | Valeur | Description   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | « EndpointDlp.dll » | Nom de la DLL DLP de point de terminaison qui fournit l’API |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | « logiciel \\ Microsoft \\ Windows Defender » | Windows Defender clé de registre sous HKLM où certains paramètres DLP de point de terminaison sont stockés |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Valeur de ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  Chemin d’accès au Registre sous la clé HKLM à partir de laquelle l’emplacement d’installation de EndpointDlp.dll peut être obtenu |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | INSTALLLOCATION | Valeur de Registre sous ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY dans laquelle l’emplacement d’installation du EndpointDlp.dll est stocké |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | systèmes | Sur les plateformes x64, concaténez ce répertoire pour obtenir la version x86 de EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Vérifier si le point de terminaison DLP est activé

Pour déterminer si le point de terminaison DLP est activé sur le système, vérifiez la valeur de clé de Registre suivante. 

| Constante | Valeur | Description   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  « \\ Fonctionnalités » | Le chemin d’accès à la clé de l’indicateur de point de terminaison activé par DLP sous (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "SenseDlpEnabled" | Valeur de Registre sous ENDPOINTDLP_ENABLED_FLAG_REGKEY contenant la clé de registre de l’indicateur DLP activé

## <a name="endpoint-dlp-apis"></a>API DLP de point de terminaison

Les tableaux suivants répertorient les API fournies par la dll DLP de point de terminaison.

### <a name="initialization-and-versioning"></a>Initialisation et contrôle de version

| API | Description |
|-----|-------------|
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.                                  |


### <a name="document-operations"></a>Opérations de document

| API | Description |
|-----|-------------|
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md) | Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture. |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md) | Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.  |
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.                                  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fournit au système des informations sur un document avant le lancement de l’opération d’ouverture.  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fournit au système des informations sur un document une fois l’opération d’ouverture terminée.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fournit au système des informations sur un document avant le lancement de l’opération de fermeture du document.                                  |

### <a name="save-as-operations"></a>Enregistrer en tant que opérations
| API | Description |
|-----|-------------|
| [DlpNotifyPreSaveAsDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fournit au système des informations sur un document avant le lancement d’une opération Enregistrer sous.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fournit au système des informations sur un document après la fin de l’opération Enregistrer sous.                                  |


### <a name="drag-and-drop-operations"></a>Opérations de glisser-déplacer

| API | Description |
|-----|-------------|
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fournit au système des informations sur un document quand une cible de déplacement est entrée.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fournit au système des informations sur un document lors de la sortie d’une cible de déplacement.                                  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération glisser-déplacer.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fournit au système des informations sur un document après l’exécution d’une opération glisser-déplacer.  |


### <a name="clipboard-operations"></a>opérations du Presse-papiers

| API | Description |
|-----|-------------|
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération copier dans le presse-papiers.  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fournit au système des informations sur un document après l’exécution d’une opération copier dans le presse-papiers.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération coller à partir du presse-papiers.  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fournit au système des informations sur un document après la fin de l’opération coller à partir du presse-papiers.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fournit au système des informations d’État après la fin d’une opération de presse-papiers.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifie le système avant l’initialisation d’une opération de presse-papiers.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Détermine si l’application doit extraire les données du presse-papiers du système au lieu de les extraire de son cache interne.                                  |

### <a name="print-operations"></a>Opérations d’impression

| API | Description |
|-----|-------------|
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fournit au système des informations sur un document avant le lancement d’une opération d’impression.  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fournit au système des informations sur un document après le démarrage d’une opération d’impression.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fournit au système des informations sur un document une fois l’opération d’impression terminée.                                  |

## <a name="endpoint-dlp-example-header"></a>En-tête d’exemple DLP de point de terminaison

étant donné que l’en-tête DLP de point de terminaison n’est pas inclus dans la SDK Windows, vous devez créer vous-même le fichier d’en-tête pour pouvoir utiliser les signatures d’API dans votre implémentation. Pour votre commodité, nous fournissons un exemple de code que vous pouvez copier et coller dans votre application. En plus des déclarations de fonction, cette liste de code définit également des constantes utiles telles que les informations de contrôle de version et les chemins de clés de registre.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


/*
Function description:
    Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.

Parameters:
    None

Return:
    TRUE if calling into the OS clipboard is mandatory, FALSE otherwise
*/
BOOL WINAPI DlpMustPasteFromSystemClipboard();

```


