---
description: 'En savoir plus sur : utilisation des hooks'
ms.assetid: f0ca9e41-a9f7-435f-a601-f0959adcb514
title: Utilisation de hooks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34539855a30a67964acfe671c29de3cacdf23314cbb51bb80027d4b388e47b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849629"
---
# <a name="using-hooks"></a>Utilisation de hooks

Les exemples de code suivants montrent comment effectuer les tâches suivantes associées aux Hooks :

-   [Installation et libération des procédures de Hook](#installing-and-releasing-hook-procedures)
-   [Surveillance des événements système](#monitoring-system-events)

## <a name="installing-and-releasing-hook-procedures"></a>Installation et libération des procédures de Hook

Vous pouvez installer une procédure de hook en appelant la fonction [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) et en spécifiant le type de raccordement appelant la procédure, si la procédure doit être associée à tous les threads dans le même bureau que le thread appelant ou avec un thread particulier, et un pointeur vers le point d’entrée de procédure.

Vous devez placer une procédure de raccordement globale dans une DLL distincte de l’application qui installe la procédure de raccordement. L’application d’installation doit disposer du handle vers le module DLL avant de pouvoir installer la procédure de Hook. Pour récupérer un handle du module DLL, appelez la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la dll. Une fois que vous avez obtenu le descripteur, vous pouvez appeler la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer un pointeur vers la procédure de raccordement. Enfin, utilisez [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) pour installer l’adresse de la procédure de raccordement dans la chaîne de raccordement appropriée. **SetWindowsHookEx** passe le handle de module, un pointeur vers le point d’entrée de procédure de hook et 0 pour l’identificateur de thread, indiquant que la procédure de raccordement doit être associée à tous les threads dans le même bureau que le thread appelant. Cette séquence est présentée dans l’exemple suivant.

``` syntax
HOOKPROC hkprcSysMsg;
static HINSTANCE hinstDLL; 
static HHOOK hhookSysMsg; 
 
hinstDLL = LoadLibrary(TEXT("c:\\myapp\\sysmsg.dll")); 
hkprcSysMsg = (HOOKPROC)GetProcAddress(hinstDLL, "SysMessageProc"); 

hhookSysMsg = SetWindowsHookEx( 
                    WH_SYSMSGFILTER,
                    hkprcSysMsg,
                    hinstDLL,
                    0); 
```

Vous pouvez libérer une procédure de raccordement spécifique au thread (supprimer son adresse de la chaîne de raccordement) en appelant la fonction [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex) , en spécifiant le handle de la procédure de raccordement à libérer. Libérer une procédure de raccordement dès que votre application n’en a plus besoin.

Vous pouvez publier une procédure de raccordement globale à l’aide de [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex), mais cette fonction ne libère pas la dll contenant la procédure de Hook. Cela est dû au fait que les procédures de hook globales sont appelées dans le contexte de processus de chaque application dans le bureau, ce qui entraîne un appel implicite à la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour tous ces processus. Étant donné qu’un appel à la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) ne peut pas être effectué pour un autre processus, il n’existe aucun moyen de libérer la dll. Le système libère ensuite la DLL une fois que tous les processus explicitement liés à la DLL se sont terminés ou ont été appelés **FreeLibrary** et que tous les processus qui ont appelé la procédure de Hook ont repris le traitement en dehors de la dll.

Une autre méthode pour installer une procédure de hook globale consiste à fournir une fonction d’installation dans la DLL, ainsi que la procédure de Hook. Avec cette méthode, l’application d’installation n’a pas besoin du handle du module DLL. En établissant une liaison avec la DLL, l’application accède à la fonction d’installation. La fonction d’installation peut fournir le descripteur du module DLL et d’autres détails dans l’appel à [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa). La DLL peut également contenir une fonction qui libère la procédure de hook globale ; l’application peut appeler cette fonction de libération de Hook lorsqu’elle se termine.

## <a name="monitoring-system-events"></a>Surveillance des événements système

L’exemple suivant utilise une variété de procédures de hook spécifiques au thread pour surveiller le système pour les événements qui affectent un thread. Il montre comment traiter les événements pour les types de procédures de raccordement suivants :

-   **WH \_ CALLWNDPROC**
-   **WH \_ CBT**
-   **WH \_ débogage**
-   **WH \_ GETMESSAGE**
-   **\_clavier WH**
-   **à \_ la souris**
-   **WH \_ msgfilter**

L’utilisateur peut installer et supprimer une procédure de hook à l’aide du menu. Lorsqu’une procédure de hook est installée et qu’un événement surveillé par la procédure se produit, la procédure écrit les informations relatives à l’événement dans la zone cliente de la fenêtre principale de l’application.


```
#include <windows.h>
#include <strsafe.h>
#include "app.h"

#pragma comment( lib, "user32.lib") 
#pragma comment( lib, "gdi32.lib")

#define NUMHOOKS 7 
 
// Global variables 
 
typedef struct _MYHOOKDATA 
{ 
    int nType; 
    HOOKPROC hkprc; 
    HHOOK hhook; 
} MYHOOKDATA; 
 
MYHOOKDATA myhookdata[NUMHOOKS]; 

HWND gh_hwndMain;

// Hook procedures

LRESULT WINAPI CallWndProc(int, WPARAM, LPARAM);
LRESULT WINAPI CBTProc(int, WPARAM, LPARAM);
LRESULT WINAPI DebugProc(int, WPARAM, LPARAM);
LRESULT WINAPI GetMsgProc(int, WPARAM, LPARAM);
LRESULT WINAPI KeyboardProc(int, WPARAM, LPARAM);
LRESULT WINAPI MouseProc(int, WPARAM, LPARAM);
LRESULT WINAPI MessageProc(int, WPARAM, LPARAM);

void LookUpTheMessage(PMSG, LPTSTR);
 
LRESULT WINAPI MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    static BOOL afHooks[NUMHOOKS]; 
    int index; 
    static HMENU hmenu; 
 
    gh_hwndMain = hwndMain;
    
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Save the menu handle
 
            hmenu = GetMenu(hwndMain); 
 
            // Initialize structures with hook data. The menu-item identifiers are 
            // defined as 0 through 6 in the header file app.h. They can be used to 
            // identify array elements both here and during the WM_COMMAND message. 
 
            myhookdata[IDM_CALLWNDPROC].nType = WH_CALLWNDPROC; 
            myhookdata[IDM_CALLWNDPROC].hkprc = CallWndProc; 
            myhookdata[IDM_CBT].nType = WH_CBT; 
            myhookdata[IDM_CBT].hkprc = CBTProc; 
            myhookdata[IDM_DEBUG].nType = WH_DEBUG; 
            myhookdata[IDM_DEBUG].hkprc = DebugProc; 
            myhookdata[IDM_GETMESSAGE].nType = WH_GETMESSAGE; 
            myhookdata[IDM_GETMESSAGE].hkprc = GetMsgProc; 
            myhookdata[IDM_KEYBOARD].nType = WH_KEYBOARD; 
            myhookdata[IDM_KEYBOARD].hkprc = KeyboardProc; 
            myhookdata[IDM_MOUSE].nType = WH_MOUSE; 
            myhookdata[IDM_MOUSE].hkprc = MouseProc; 
            myhookdata[IDM_MSGFILTER].nType = WH_MSGFILTER; 
            myhookdata[IDM_MSGFILTER].hkprc = MessageProc; 
 
            // Initialize all flags in the array to FALSE. 
 
            memset(afHooks, FALSE, sizeof(afHooks)); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                 // The user selected a hook command from the menu. 
 
                case IDM_CALLWNDPROC: 
                case IDM_CBT: 
                case IDM_DEBUG: 
                case IDM_GETMESSAGE: 
                case IDM_KEYBOARD: 
                case IDM_MOUSE: 
                case IDM_MSGFILTER: 
 
                    // Use the menu-item identifier as an index 
                    // into the array of structures with hook data. 
 
                    index = LOWORD(wParam); 
 
                    // If the selected type of hook procedure isn't 
                    // installed yet, install it and check the 
                    // associated menu item. 
 
                    if (!afHooks[index]) 
                    { 
                        myhookdata[index].hhook = SetWindowsHookEx( 
                            myhookdata[index].nType, 
                            myhookdata[index].hkprc, 
                            (HINSTANCE) NULL, GetCurrentThreadId()); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_CHECKED); 
                        afHooks[index] = TRUE; 
                    } 
 
                    // If the selected type of hook procedure is 
                    // already installed, remove it and remove the 
                    // check mark from the associated menu item. 
 
                    else 
                    { 
                        UnhookWindowsHookEx(myhookdata[index].hhook); 
                        CheckMenuItem(hmenu, index, 
                            MF_BYCOMMAND | MF_UNCHECKED); 
                        afHooks[index] = FALSE; 
                    } 
 
                default: 
                    return (DefWindowProc(hwndMain, uMsg, wParam, 
                        lParam)); 
            } 
            break; 
 
            //
            // Process other messages. 
            //
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
/**************************************************************** 
  WH_CALLWNDPROC hook procedure 
 ****************************************************************/ 
 
LRESULT WINAPI CallWndProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szCWPBuf[256]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch;
    HRESULT hResult; 
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szCWPBuf, 256/sizeof(TCHAR),  
               "CALLWNDPROC - tsk: %ld, msg: %s, %d times   ", 
                wParam, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: writer error handler
            }
            hResult = StringCchLength(szCWPBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 15, szCWPBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CALLWNDPROC].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_GETMESSAGE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK GetMsgProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szMSGBuf[256]; 
    CHAR szRem[16]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0) // do not process message 
        return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case HC_ACTION: 
            switch (wParam) 
            { 
                case PM_REMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_REMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                case PM_NOREMOVE:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "PM_NOREMOVE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
 
                default:
                    hResult = StringCchCopy(szRem, 16/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    break; 
            } 
 
            // Call an application-defined function that converts a 
            // message constant to a string and copies it to a 
            // buffer. 
 
            LookUpTheMessage((PMSG) lParam, szMsg); 
 
            hdc = GetDC(gh_hwndMain);
            hResult = StringCchPrintf(szMSGBuf, 256/sizeof(TCHAR), 
                "GETMESSAGE - wParam: %s, msg: %s, %d times   ", 
                szRem, szMsg, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szMSGBuf, 256/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 35, szMSGBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_GETMESSAGE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_DEBUG hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK DebugProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HC_ACTION:
            hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),   
                "DEBUG - nCode: %d, tsk: %ld, %d times   ", 
                nCode,wParam, c++);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            }
            hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
            if (FAILED(hResult))
            {
            // TODO: write error handler
            } 
            TextOut(hdc, 2, 55, szBuf, cch); 
            break; 
 
        default: 
            break; 
    } 
 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_DEBUG].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_CBT hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK CBTProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szCode[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, 
            lParam); 
 
    hdc = GetDC(gh_hwndMain); 
 
    switch (nCode) 
    { 
        case HCBT_ACTIVATE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_ACTIVATE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CLICKSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CLICKSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_CREATEWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_CREATEWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_DESTROYWND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_DESTROYWND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_KEYSKIPPED:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_KEYSKIPPED");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MINMAX:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MINMAX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_MOVESIZE:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_MOVESIZE");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_QS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_QS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SETFOCUS:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SETFOCUS");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case HCBT_SYSCOMMAND:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "HCBT_SYSCOMMAND");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchCopy(szCode, 128/sizeof(TCHAR), "Unknown");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
    } 
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "CBT -  nCode: %s, tsk: %ld, %d times   ",
        szCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 75, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_CBT].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MOUSE hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MouseProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process the message 
        return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, 
            wParam, lParam); 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), 
        "MOUSE - nCode: %d, msg: %s, x: %d, y: %d, %d times   ", 
        nCode, szMsg, LOWORD(lParam), HIWORD(lParam), c++); 
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
    TextOut(hdc, 2, 95, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MOUSE].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_KEYBOARD hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK KeyboardProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, 
            wParam, lParam); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR), "KEYBOARD - nCode: %d, vk: %d, %d times ", nCode, wParam, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 115, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_KEYBOARD].hhook, nCode, wParam, lParam); 
} 
 
/**************************************************************** 
  WH_MSGFILTER hook procedure 
 ****************************************************************/ 
 
LRESULT CALLBACK MessageProc(int nCode, WPARAM wParam, LPARAM lParam) 
{ 
    CHAR szBuf[128]; 
    CHAR szMsg[16]; 
    CHAR szCode[32]; 
    HDC hdc; 
    static int c = 0; 
    size_t cch; 
    HRESULT hResult;
 
    if (nCode < 0)  // do not process message 
        return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, 
            wParam, lParam); 
 
    switch (nCode) 
    { 
        case MSGF_DIALOGBOX:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_DIALOGBOX");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_MENU:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_MENU");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        case MSGF_SCROLLBAR:
            hResult = StringCchCopy(szCode, 32/sizeof(TCHAR), "MSGF_SCROLLBAR");
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
            break; 
 
        default:
            hResult = StringCchPrintf(szCode, 128/sizeof(TCHAR), "Unknown: %d", nCode);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    }
            break; 
    } 
 
    // Call an application-defined function that converts a message 
    // constant to a string and copies it to a buffer. 
 
    LookUpTheMessage((PMSG) lParam, szMsg); 
 
    hdc = GetDC(gh_hwndMain);
    hResult = StringCchPrintf(szBuf, 128/sizeof(TCHAR),  
        "MSGFILTER  nCode: %s, msg: %s, %d times    ", 
        szCode, szMsg, c++);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    hResult = StringCchLength(szBuf, 128/sizeof(TCHAR), &cch);
    if (FAILED(hResult))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, 2, 135, szBuf, cch); 
    ReleaseDC(gh_hwndMain, hdc); 
    
    return CallNextHookEx(myhookdata[IDM_MSGFILTER].hhook, nCode, wParam, lParam); 
}
```



 

 
