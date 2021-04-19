---
description: Gestion des erreurs dans Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Gestion des erreurs Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516003"
---
# <a name="handling-winsock-errors"></a><span data-ttu-id="b58bc-103">Gestion des erreurs Winsock</span><span class="sxs-lookup"><span data-stu-id="b58bc-103">Handling Winsock Errors</span></span>

<span data-ttu-id="b58bc-104">La plupart des fonctions Windows Sockets 2 ne retournent pas la cause spécifique d’une erreur quand la fonction retourne.</span><span class="sxs-lookup"><span data-stu-id="b58bc-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="b58bc-105">Certaines fonctions Winsock retournent la valeur zéro en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="b58bc-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="b58bc-106">Dans le cas contraire, l’erreur de SOCKET de valeur \_ (-1) est retournée et un numéro d’erreur spécifique peut être récupéré en appelant la fonction [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="b58bc-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="b58bc-107">Pour les fonctions Winsock qui renvoient un descripteur, une valeur de retour de socket non valide \_ (0xFFFF) indique une erreur et un numéro d’erreur spécifique peut être récupéré en appelant **WSAGetLastError**.</span><span class="sxs-lookup"><span data-stu-id="b58bc-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="b58bc-108">Pour les fonctions Winsock qui retournent un pointeur, une valeur de retour **null** indique une erreur et un numéro d’erreur spécifique peut être récupéré en appelant la fonction **WSAGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="b58bc-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="b58bc-109">Un code d’erreur Winsock peut être converti en HRESULT pour une utilisation dans un appel de procédure distante (RPC) à l’aide \_ de HRESULT à partir de \_ Win32.</span><span class="sxs-lookup"><span data-stu-id="b58bc-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="b58bc-110">Dans les versions antérieures du kit de développement logiciel (SDK) de la plateforme, HRESULT \_ de \_ Win32 était défini en tant que macro dans le fichier d’en-tête *winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="b58bc-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="b58bc-111">Dans le kit de développement logiciel (SDK) Microsoft Windows, HRESULT \_ de \_ Win32 est défini en tant que fonction inline dans le fichier d’en-tête *winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="b58bc-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b58bc-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b58bc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b58bc-113">Codes d’erreur de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b58bc-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



