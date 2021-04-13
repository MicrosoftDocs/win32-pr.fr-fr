---
title: Utilisation de la boîte de dialogue connexions
description: La fonction WNetConnectionDialog crée une boîte de dialogue qui permet à l’utilisateur de parcourir les ressources réseau et de s’y connecter.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315683"
---
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="1a962-103">Utilisation de la boîte de dialogue connexions</span><span class="sxs-lookup"><span data-stu-id="1a962-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="1a962-104">La fonction [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crée une boîte de dialogue qui permet à l’utilisateur de parcourir les ressources réseau et de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="1a962-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="1a962-105">Vous pouvez également appeler la fonction [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) pour créer une boîte de dialogue de connexion.</span><span class="sxs-lookup"><span data-stu-id="1a962-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="1a962-106">**WNetConnectionDialog1** requiert une structure [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .</span><span class="sxs-lookup"><span data-stu-id="1a962-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="1a962-107">La fonction [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crée une boîte de dialogue qui permet à l’utilisateur de se déconnecter des ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="1a962-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="1a962-108">L’exemple de code suivant montre comment appeler la fonction **WNetConnectionDialog** pour créer une boîte de dialogue qui affiche les ressources de disque.</span><span class="sxs-lookup"><span data-stu-id="1a962-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="1a962-109">Si l’appel échoue, l’exemple appelle un gestionnaire d’erreurs défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="1a962-109">If the call fails, the sample calls an application-defined error handler.</span></span>


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



<span data-ttu-id="1a962-110">Pour plus d’informations sur l’utilisation d’un gestionnaire d’erreurs défini par l’application, consultez [récupération des erreurs réseau](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1a962-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 