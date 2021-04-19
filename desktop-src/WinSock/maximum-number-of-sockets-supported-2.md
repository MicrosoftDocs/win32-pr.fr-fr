---
description: Le nombre maximal de sockets pris en charge par un fournisseur de services Windows Sockets particulier est spécifique à l’implémentation.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Nombre maximal de sockets pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515024"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="222a7-103">Nombre maximal de sockets pris en charge</span><span class="sxs-lookup"><span data-stu-id="222a7-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="222a7-104">Le nombre maximal de sockets pris en charge par un fournisseur de services Windows Sockets particulier est spécifique à l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="222a7-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="222a7-105">Le fournisseur Microsoft Winsock limite le nombre maximal de sockets pris en charge uniquement par la mémoire disponible sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="222a7-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="222a7-106">Toutefois, les fournisseurs Winsock tiers peuvent avoir des limitations sur le nombre de sockets pris en charge.</span><span class="sxs-lookup"><span data-stu-id="222a7-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="222a7-107">Une application ne doit pas faire d’hypothèses sur la disponibilité d’un certain nombre de Sockets.</span><span class="sxs-lookup"><span data-stu-id="222a7-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="222a7-108">Pour plus d’informations sur cette rubrique, consultez [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="222a7-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="222a7-109">FD \_ set et SELECT</span><span class="sxs-lookup"><span data-stu-id="222a7-109">FD\_SET and select</span></span>

<span data-ttu-id="222a7-110">Un certain nombre de \_ macros FD xxx sont définies dans le fichier d’en-tête *Winsock2. h* pour une utilisation dans le portage d’applications vers Windows à partir de l’environnement UNIX.</span><span class="sxs-lookup"><span data-stu-id="222a7-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="222a7-111">Ces macros sont utilisées avec les fonctions [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) et [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) pour le portage d’applications vers Windows.</span><span class="sxs-lookup"><span data-stu-id="222a7-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="222a7-112">Le nombre maximal de sockets qu’une application Windows Sockets peut utiliser n’est pas affecté par la constante de manifeste FD \_ .</span><span class="sxs-lookup"><span data-stu-id="222a7-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="222a7-113">Cette valeur définie dans le fichier d’en-tête *Winsock2. h* est utilisée lors de la construction des structures [**FD \_ Set**](/windows/desktop/api/winsock/nf-winsock-fd_set) utilisées avec la fonction **Select** .</span><span class="sxs-lookup"><span data-stu-id="222a7-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="222a7-114">La valeur par défaut dans Winsock2. h est 64.</span><span class="sxs-lookup"><span data-stu-id="222a7-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="222a7-115">Si une application est conçue pour pouvoir travailler avec plus de 64 sockets à l’aide des fonctions **Select** et **WSAPoll** , l’implémenteur doit définir la fonction FD \_ de manifeste dans chaque fichier source avant d’inclure le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="222a7-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="222a7-116">L’une des méthodes possibles consiste à inclure la définition dans les options du compilateur dans le Makefile.</span><span class="sxs-lookup"><span data-stu-id="222a7-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="222a7-117">Par exemple, vous pouvez ajouter « -DFD \_ deinstall = 128 » comme option à la ligne de commande du compilateur pour Microsoft C++.</span><span class="sxs-lookup"><span data-stu-id="222a7-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="222a7-118">Il faut insister sur le fait que \_ la définition de FD configure en tant que valeur particulière n’a aucun effet sur le nombre réel de sockets fournis par un fournisseur de services Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="222a7-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="222a7-119">Cette valeur affecte uniquement les \_ macros FD xxx utilisées par les fonctions **Select** et **WSAPoll** .</span><span class="sxs-lookup"><span data-stu-id="222a7-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="222a7-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="222a7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="222a7-121">**\_ensemble FD**</span><span class="sxs-lookup"><span data-stu-id="222a7-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="222a7-122">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="222a7-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="222a7-123">**sélectionné**</span><span class="sxs-lookup"><span data-stu-id="222a7-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="222a7-124">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="222a7-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="222a7-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="222a7-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="222a7-126">**WSAPoll**</span><span class="sxs-lookup"><span data-stu-id="222a7-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
