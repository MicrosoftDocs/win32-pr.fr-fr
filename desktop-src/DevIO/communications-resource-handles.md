---
description: Un processus utilise la fonction CreateFile pour ouvrir un handle vers une ressource de communication.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Descripteurs de ressources de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393087"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="13d4a-103">Descripteurs de ressources de communication</span><span class="sxs-lookup"><span data-stu-id="13d4a-103">Communications Resource Handles</span></span>

<span data-ttu-id="13d4a-104">Un processus utilise la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle vers une ressource de communication.</span><span class="sxs-lookup"><span data-stu-id="13d4a-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="13d4a-105">Par exemple, si vous spécifiez COM1, un handle est ouvert à un port série et LPT1 ouvre un handle vers un port parallèle.</span><span class="sxs-lookup"><span data-stu-id="13d4a-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="13d4a-106">Si la ressource spécifiée est actuellement utilisée par un autre processus, **CreateFile** échoue.</span><span class="sxs-lookup"><span data-stu-id="13d4a-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="13d4a-107">Tout thread du processus peut utiliser le handle retourné par **CreateFile** pour identifier la ressource dans toutes les fonctions qui accèdent à la ressource.</span><span class="sxs-lookup"><span data-stu-id="13d4a-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="13d4a-108">Lorsque le processus appelle [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir une ressource de communication, il spécifie les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="13d4a-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="13d4a-109">Quel type d’accès en lecture/écriture existe pour la ressource spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13d4a-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="13d4a-110">Indique si le handle peut être hérité par les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="13d4a-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="13d4a-111">Indique si le handle peut être utilisé dans les opérations d’e/s (asynchrones) avec chevauchement.</span><span class="sxs-lookup"><span data-stu-id="13d4a-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="13d4a-112">(Pour obtenir une description des opérations avec chevauchement, consultez [Synchronization](/windows/desktop/Sync/synchronization).)</span><span class="sxs-lookup"><span data-stu-id="13d4a-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="13d4a-113">Lorsque le processus utilise [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir une ressource de communication, il doit spécifier certaines valeurs pour les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="13d4a-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="13d4a-114">Le paramètre *fdwShareMode* doit être égal à zéro, ouvrant la ressource pour un accès exclusif.</span><span class="sxs-lookup"><span data-stu-id="13d4a-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="13d4a-115">Le paramètre *fdwCreate* doit spécifier l' \_ indicateur Open Existing.</span><span class="sxs-lookup"><span data-stu-id="13d4a-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="13d4a-116">Le paramètre *hTemplateFile* doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="13d4a-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="13d4a-117">Quand vous utilisez [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir un handle directement sur un appareil, une application doit utiliser les caractères spéciaux « \\ \\ . \\ » pour identifier l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13d4a-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="13d4a-118">Par exemple, pour ouvrir un handle pour le pilote A, spécifiez \\ \\ . \\ r : pour le paramètre *lpszName* de **CreateFile**.</span><span class="sxs-lookup"><span data-stu-id="13d4a-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="13d4a-119">Le processus appelant peut utiliser le descripteur dans la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) pour envoyer des codes de contrôle à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13d4a-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
