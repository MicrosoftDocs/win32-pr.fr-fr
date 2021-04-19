---
title: Utilisation de la copie de données
description: Cette rubrique fournit un exemple qui montre comment envoyer des informations entre deux applications.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Interface utilisateur Windows, copie de données
- copie de données, exemples
- copie de données, message de WM_COPYDATA
- Message WM_COPYDATA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511691"
---
# <a name="using-data-copy"></a><span data-ttu-id="0286e-107">Utilisation de la copie de données</span><span class="sxs-lookup"><span data-stu-id="0286e-107">Using Data Copy</span></span>

<span data-ttu-id="0286e-108">L’exemple suivant montre comment envoyer des informations entre deux applications à l’aide du message [**WM \_ COPYDATA**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="0286e-108">The following example demonstrates how to send information between two applications using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span>

<span data-ttu-id="0286e-109">L’application émettrice affiche une boîte de dialogue à l’utilisateur qui demande certaines informations.</span><span class="sxs-lookup"><span data-stu-id="0286e-109">The sending application displays a dialog box to the user which requests certain information.</span></span> <span data-ttu-id="0286e-110">L’application empaquette les informations dans une structure de données privée, comprend un pointeur vers la structure dans la structure [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) et envoie les informations à l’application réceptrice à l’aide du message [**WM \_ COPYDATA**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="0286e-110">The application packages the information into a private data structure, includes a pointer to the structure in the [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure, and sends the information to the receiving application using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <span data-ttu-id="0286e-111">L’application réceptrice a une fenêtre masquée avec le nom de la classe Disp32Class.</span><span class="sxs-lookup"><span data-stu-id="0286e-111">The receiving application has a hidden window with the class name Disp32Class.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



<span data-ttu-id="0286e-112">L’application réceptrice a une fenêtre masquée qui reçoit les informations de [**WM \_ COPYDATA**](wm-copydata.md) et les affiche pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0286e-112">The receiving application has a hidden window which receives the information from [**WM\_COPYDATA**](wm-copydata.md) and displays it to the user.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a><span data-ttu-id="0286e-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0286e-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0286e-114">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="0286e-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0286e-115">**FindWindow**</span><span class="sxs-lookup"><span data-stu-id="0286e-115">**FindWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 