---
description: Point d’entrée facultatif dans une bibliothèque de liens dynamiques (DLL). Lorsque le système démarre ou termine un processus ou un thread, il appelle la fonction de point d’entrée pour chaque DLL chargée à l’aide du premier thread du processus.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: Point d’entrée DllMain (Process. h)
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007462"
---
# <a name="dllmain-entry-point"></a>Point d’entrée DllMain

Point d’entrée facultatif dans une bibliothèque de liens dynamiques (DLL). Lorsque le système démarre ou termine un processus ou un thread, il appelle la fonction de point d’entrée pour chaque DLL chargée à l’aide du premier thread du processus. Le système appelle également la fonction de point d’entrée pour une DLL lorsqu’elle est chargée ou déchargée à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="example"></a>Exemple

```cpp
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

Il s’agit d’un exemple de la [bibliothèque de liens dynamiques Entry-Point fonction](dynamic-link-library-entry-point-function.md).


> [!WARNING]
> Il existe des limites significatives sur ce que vous pouvez faire en toute sécurité dans un point d’entrée de DLL. consultez les [meilleures pratiques générales](dynamic-link-library-best-practices.md) pour des api Windows spécifiques qui ne peuvent pas être appelées dans DllMain. Si vous n’avez besoin que de l’initialisation la plus simple, faites-le dans une fonction d’initialisation pour la DLL. Vous pouvez demander aux applications d’appeler la fonction d’initialisation après l’exécution de DllMain et avant d’appeler d’autres fonctions dans la DLL.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hinstDLL* \[ dans\]
</dt> <dd>

Handle du module DLL. La valeur est l’adresse de base de la DLL. Le **HINSTANCE** d’une dll est le même que le **HMODULE** de la dll. par conséquent, *hinstDLL* peut être utilisé dans les appels aux fonctions qui requièrent un handle de module.

</dd> <dt>

*fdwReason* \[ dans\]
</dt> <dd>

Code de raison qui indique la raison pour laquelle la fonction de point d’entrée de la DLL est appelée. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**Dll \_ \_Attachement de processus**</dt> <dt>1</dt> </dl> | La DLL est chargée dans l’espace d’adressage virtuel du processus en cours suite au démarrage du processus ou à la suite d’un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Les dll peuvent utiliser cette opportunité pour initialiser toutes les données d’instance ou pour utiliser la fonction [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) pour allouer un index de stockage local des threads (TLS).<br/> Le paramètre *lpReserved* indique si la dll est chargée de manière statique ou dynamique.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Dll \_ \_Détacher le processus**</dt> <dt>0</dt> </dl> | La DLL est déchargée de l’espace d’adressage virtuel du processus appelant, car elle a été chargée sans succès ou le décompte de références a atteint zéro (les processus se sont terminés ou s’ils ont été appelés [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) une seule fois pour chaque fois que ce dernier appelle [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).<br/> Le paramètre *lpReserved* indique si la dll est déchargée suite à un appel [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , à un échec de chargement ou à un arrêt de processus.<br/> La DLL peut utiliser cette opportunité pour appeler la fonction [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) afin de libérer les index TLS alloués à l’aide de [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) et libérer les données locales du thread.<br/> Notez que le thread qui reçoit la notification de **\_ \_ détachement de processus dll** n’est pas nécessairement le même que celui qui a reçu la notification d' **\_ \_ attachement de processus dll** .<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**Dll \_ \_Attachement de thread**</dt> <dt>2</dt> </dl>    | Le processus en cours crée un nouveau thread. Dans ce cas, le système appelle la fonction de point d’entrée de toutes les dll actuellement attachées au processus. L’appel est effectué dans le contexte du nouveau thread. Les dll peuvent utiliser cette opportunité pour initialiser un emplacement TLS pour le thread. Un thread qui appelle la fonction de point d’entrée DLL avec l' **\_ \_ attachement de processus dll** n’appelle pas la fonction de point d’entrée dll avec l' **attachement de \_ thread \_ de dll**. <br/> Notez que la fonction de point d’entrée d’une DLL est appelée avec cette valeur uniquement par les threads créés après le chargement de la DLL par le processus. Quand une DLL est chargée à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), les threads existants n’appellent pas la fonction de point d’entrée de la dll nouvellement chargée.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**Dll \_ \_Détachement de thread**</dt> <dt>3</dt> </dl>    | Un thread s’arrête correctement. Si la DLL a stocké un pointeur vers la mémoire allouée dans un emplacement TLS, elle doit utiliser cette opportunité pour libérer de la mémoire. Le système appelle la fonction de point d’entrée de toutes les dll actuellement chargées avec cette valeur. L’appel est effectué dans le contexte du thread de sortie.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[ dans\]
</dt> <dd>

Si *fdwReason* est **un \_ \_ attachement de processus dll**, *lpvReserved* a la **valeur null** pour les charges dynamiques et non null pour les charges statiques.

Si *fdwReason* est **un \_ processus de \_ détachement de dll**, *lpvReserved* a la **valeur null** si [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) a été appelé ou si le chargement de la dll a échoué et n’a pas la **valeur null** si le processus se termine.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Lorsque le système appelle la fonction **DllMain** avec la valeur d' **\_ \_ attachement du processus dll** , la fonction retourne **true** si elle réussit ou **false** si l’initialisation échoue. Si la valeur de retour est **false** lorsque **DllMain** est appelé, car le processus utilise la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , **LoadLibrary** retourne la valeur null. (Le système appelle immédiatement votre fonction de point d’entrée avec le **\_ \_ détachement de processus dll** et décharge la dll.) Si la valeur de retour est **false** lorsque **DllMain** est appelé pendant l’initialisation du processus, le processus se termine avec une erreur. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Lorsque le système appelle la fonction **DllMain** avec une valeur autre que le **processus d' \_ \_ attachement de dll**, la valeur de retour est ignorée.

## <a name="remarks"></a>Notes

**DllMain** est un espace réservé pour le nom de la fonction définie par la bibliothèque. Vous devez spécifier le nom réel que vous utilisez lorsque vous générez votre DLL. Pour plus d’informations, consultez la documentation fournie avec vos outils de développement.

Lors du démarrage initial du processus ou après un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), le système analyse la liste des DLL chargées pour le processus. Pour chaque DLL qui n’a pas encore été appelée avec la valeur d' **\_ \_ attachement du processus dll** , le système appelle la fonction de point d’entrée de la dll. Cet appel est effectué dans le contexte du thread qui a provoqué la modification de l’espace d’adressage du processus, par exemple le thread principal du processus ou le thread qui a appelé **LoadLibrary**. L’accès au point d’entrée est sérialisé par le système à l’échelle du processus. Les threads dans *DllMain* maintiennent le verrou du chargeur, de sorte qu’aucune dll supplémentaire ne peut être chargée ou initialisée dynamiquement.

Si la fonction de point d’entrée de la DLL retourne la valeur FALSe après une notification d' **\_ \_ attachement de processus dll** , elle reçoit une notification de **\_ \_ détachement de processus dll** et la dll est déchargée immédiatement. Toutefois, si le code d' **\_ \_ attachement du processus dll** lève une exception, la fonction de point d’entrée ne recevra pas la notification de **\_ \_ détachement de processus dll** .

Dans certains cas, la fonction de point d’entrée est appelée pour un thread de fin même si la fonction de point d’entrée n’a jamais été appelée avec l' **\_ \_ attachement de thread de dll** pour le thread :

-   Le thread était le thread initial dans le processus, donc le système a appelé la fonction de point d’entrée avec la valeur d' **\_ \_ attachement du processus dll** .
-   Le thread était déjà en cours d’exécution lorsqu’un appel à la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) a été effectué, de sorte que le système n’a jamais appelé la fonction de point d’entrée pour celui-ci.

Lorsqu’une DLL est déchargée d’un processus suite à un échec de chargement de la DLL, à l’arrêt du processus ou à un appel à [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), le système n’appelle pas la fonction de point d’entrée de la dll avec la valeur de **\_ \_ détachement de thread dll** pour les threads individuels du processus. La DLL n’est envoyée qu’à une notification de **\_ \_ détachement de processus dll** . Les dll peuvent profiter de cette opportunité pour nettoyer toutes les ressources de tous les threads connus de la DLL.

Lors du traitement du **\_ \_ détachement du processus DLL**, une dll ne doit libérer des ressources telles que la mémoire du tas que si la dll est déchargée dynamiquement (le paramètre *lpReserved* a la **valeur null**). Si le processus se termine (le paramètre *lpvReserved* n’a pas la **valeur null**), tous les threads du processus, à l’exception du thread actuel, se sont déjà fermés ou ont été arrêtés explicitement par un appel à la fonction [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) , ce qui peut entraîner des ressources de processus telles que des segments de mémoire dans un état incohérent. Dans ce cas, il n’est pas sûr que la DLL nettoie les ressources. Au lieu de cela, la DLL doit permettre au système d’exploitation de libérer de la mémoire.

Si vous arrêtez un processus en appelant [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) ou [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), les dll de ce processus ne reçoivent pas de notifications de **\_ \_ détachement de processus dll** . Si vous arrêtez un thread en appelant [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), les dll de ce thread ne reçoivent pas de notifications de **\_ \_ détachement de thread dll** .

La fonction de point d’entrée doit effectuer uniquement des tâches d’initialisation ou d’arrêt simples. Elle ne doit pas appeler la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ou une fonction qui appelle ces fonctions), car cela peut créer des boucles de dépendance dans l’ordre de chargement de la dll. Cela peut entraîner l’utilisation d’une DLL avant l’exécution du code d’initialisation du système. De même, la fonction de point d’entrée ne doit pas appeler la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (ou une fonction qui appelle **FreeLibrary**) pendant l’arrêt du processus, car cela peut entraîner l’utilisation d’une dll après l’exécution du code d’arrêt du système.

Étant donné que le chargement de Kernel32.dll est garanti dans l’espace d’adressage de processus lorsque la fonction de point d’entrée est appelée, l’appel de fonctions dans Kernel32.dll n’entraîne pas l’utilisation de la DLL avant l’exécution de son code d’initialisation. Par conséquent, la fonction de point d’entrée peut appeler des fonctions dans Kernel32.dll qui ne chargent pas d’autres dll. Par exemple, *DllMain* peut créer des [objets de synchronisation](/windows/desktop/Sync/synchronization-objects) , tels que des sections critiques et des MUTEX, et utiliser TLS. Malheureusement, il n’existe pas de liste exhaustive des fonctions sécurisées dans Kernel32.dll.

L’appel de fonctions qui requièrent des dll autres que Kernel32.dll peut entraîner des problèmes difficiles à diagnostiquer. Par exemple, l’appel de fonctions d’utilisateur, de Shell et COM peut entraîner des erreurs de violation d’accès, car certaines fonctions chargent d’autres composants système. Inversement, l’appel de fonctions telles que celles-ci pendant l’arrêt peut entraîner des erreurs de violation d’accès, car le composant correspondant a peut-être déjà été déchargé ou non initialisé.

Étant donné que les notifications de DLL sont sérialisées, les fonctions de point d’entrée ne doivent pas tenter de communiquer avec d’autres threads ou processus. Des blocages peuvent se produire en conséquence.

Pour plus d’informations sur les meilleures pratiques lors de l’écriture d’une DLL, consultez https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Si votre DLL est liée à la bibliothèque Runtime C (CRT), le point d’entrée fourni par le CRT appelle les constructeurs et les destructeurs pour les objets C++ globaux et statiques. Par conséquent, ces restrictions pour *DllMain* s’appliquent également aux constructeurs et aux destructeurs et tout code qui est appelé à partir de ceux-ci.

Envisagez d’appeler [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) lors de la réception d’un **\_ \_ attachement de processus dll**, à moins que votre dll soit liée à la bibliothèque Runtime C statique (CRT).


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonction de Entry-Point de bibliothèque de liens dynamiques](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[Fonctions de bibliothèque de liens dynamiques](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
