---
title: Énumération des ressources réseau
description: L’exemple suivant illustre une fonction définie par l’application (EnumerateFunc) qui énumère toutes les ressources sur un réseau.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382298"
---
# <a name="enumerating-network-resources"></a><span data-ttu-id="92197-103">Énumération des ressources réseau</span><span class="sxs-lookup"><span data-stu-id="92197-103">Enumerating Network Resources</span></span>

<span data-ttu-id="92197-104">L’exemple suivant illustre une fonction définie par l’application (EnumerateFunc) qui énumère toutes les ressources sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="92197-104">The following example illustrates an application-defined function (EnumerateFunc) that enumerates all the resources on a network.</span></span> <span data-ttu-id="92197-105">L’exemple spécifie la **valeur null** pour le pointeur vers la structure Resource, car quand [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) reçoit un pointeur **null** , il récupère un handle vers la racine du réseau. [](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)</span><span class="sxs-lookup"><span data-stu-id="92197-105">The sample specifies **NULL** for the pointer to the [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure because when [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) receives a **NULL** pointer, it retrieves a handle to the root of the network.</span></span>

<span data-ttu-id="92197-106">Pour commencer l’énumération d’une ressource de conteneur réseau, votre application doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="92197-106">To begin the enumeration of a network container resource, your application should perform the following steps:</span></span>

1.  <span data-ttu-id="92197-107">Transmettez l’adresse d’une structure [**Resource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) qui représente la ressource à la fonction [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .</span><span class="sxs-lookup"><span data-stu-id="92197-107">Pass the address of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure that represents the resource to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function.</span></span>
2.  <span data-ttu-id="92197-108">Allouez une mémoire tampon suffisamment grande pour contenir le tableau de structures [**Resources**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) retourné par la fonction [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) , ainsi que les chaînes auxquelles leurs membres pointent.</span><span class="sxs-lookup"><span data-stu-id="92197-108">Allocate a buffer large enough to hold the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures that the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function returns, plus the strings to which their members point.</span></span>
3.  <span data-ttu-id="92197-109">Transmettez le descripteur de ressource retourné par [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) à la fonction [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) .</span><span class="sxs-lookup"><span data-stu-id="92197-109">Pass the resource handle returned by [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) to the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function.</span></span>
4.  <span data-ttu-id="92197-110">Fermez le descripteur de ressource lorsqu’il n’est plus nécessaire en appelant la fonction [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) .</span><span class="sxs-lookup"><span data-stu-id="92197-110">Close the resource handle when it is no longer needed by calling the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) function.</span></span>

<span data-ttu-id="92197-111">Vous pouvez poursuivre l’énumération d’une ressource de conteneur décrite dans le tableau des structures [**Resources**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) extraites par [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span><span class="sxs-lookup"><span data-stu-id="92197-111">You can continue enumerating a container resource described in the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures retrieved by [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span></span> <span data-ttu-id="92197-112">Si le membre **dwUsage** de la structure **Resource** est égal au \_ conteneur RESOURCEUSAGE, transmettez l’adresse de la structure à la fonction [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) pour ouvrir le conteneur et poursuivre l’énumération.</span><span class="sxs-lookup"><span data-stu-id="92197-112">If the **dwUsage** member of the **NETRESOURCE** structure is equal to RESOURCEUSAGE\_CONTAINER, pass the address of the structure to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to open the container and continue the enumeration.</span></span> <span data-ttu-id="92197-113">Si **dwUsage** est égal à RESOURCEUSAGE \_ connectable, l’application peut passer l’adresse de la structure à la fonction [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) ou à la fonction [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) pour se connecter à la ressource.</span><span class="sxs-lookup"><span data-stu-id="92197-113">If **dwUsage** is equal to RESOURCEUSAGE\_CONNECTABLE, the application can pass the structure's address to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function to connect to the resource.</span></span>

<span data-ttu-id="92197-114">Tout d’abord, l’exemple appelle la fonction [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) pour commencer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="92197-114">First the sample calls the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to begin the enumeration.</span></span> <span data-ttu-id="92197-115">L’exemple appelle la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) pour allouer la mémoire tampon requise, puis appelle la fonction [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) pour définir le contenu de la mémoire tampon sur zéro.</span><span class="sxs-lookup"><span data-stu-id="92197-115">The sample calls the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function to allocate the required buffer, and then calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to set the buffer contents to zero.</span></span> <span data-ttu-id="92197-116">L’exemple appelle ensuite la fonction [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) pour continuer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="92197-116">Then the sample calls the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function to continue the enumeration.</span></span> <span data-ttu-id="92197-117">Chaque fois que le membre **dwUsage** d’une structure [**netressource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) récupérée par **WNETENUMRESOURCE** est égal au \_ conteneur RESOURCEUSAGE, la fonction EnumerateFunc s’appelle elle-même de manière récursive et utilise un pointeur vers cette structure dans son appel à **WNetOpenEnum**.</span><span class="sxs-lookup"><span data-stu-id="92197-117">Whenever the **dwUsage** member of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure retrieved by **WNetEnumResource** is equal to RESOURCEUSAGE\_CONTAINER, the EnumerateFunc function calls itself recursively and uses a pointer to that structure in its call to **WNetOpenEnum**.</span></span> <span data-ttu-id="92197-118">Enfin, l’exemple appelle la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) pour libérer la mémoire allouée, et [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) pour terminer l’énumération.</span><span class="sxs-lookup"><span data-stu-id="92197-118">Finally, the sample calls the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function to free the allocated memory, and the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) to end the enumeration.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



<span data-ttu-id="92197-119">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="92197-119">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 