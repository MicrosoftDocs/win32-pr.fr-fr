---
description: Chaque canal nommé a un nom unique qui le distingue des autres canaux nommés de la liste des systèmes des objets nommés. Un serveur de canaux spécifie un nom pour le canal lorsqu’il appelle la fonction CreateNamedPipe pour créer une ou plusieurs instances d’un canal nommé.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Noms de canaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545076"
---
# <a name="pipe-names"></a><span data-ttu-id="ebeed-104">Noms de canaux</span><span class="sxs-lookup"><span data-stu-id="ebeed-104">Pipe Names</span></span>

<span data-ttu-id="ebeed-105">Chaque canal nommé a un nom unique qui le distingue des autres canaux nommés dans la liste des objets nommés du système.</span><span class="sxs-lookup"><span data-stu-id="ebeed-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="ebeed-106">Un serveur de canaux spécifie un nom pour le canal lorsqu’il appelle la fonction [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) pour créer une ou plusieurs instances d’un canal nommé.</span><span class="sxs-lookup"><span data-stu-id="ebeed-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="ebeed-107">Les clients de canal spécifient le nom du canal lorsqu’ils appellent la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) pour se connecter à une instance du canal nommé.</span><span class="sxs-lookup"><span data-stu-id="ebeed-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="ebeed-108">Utilisez la forme suivante quand vous spécifiez le nom d’un canal dans la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :</span><span class="sxs-lookup"><span data-stu-id="ebeed-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="ebeed-109">\\\\*Nom du serveur* \\ canal \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="ebeed-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="ebeed-110">où *ServerName* est le nom d’un ordinateur distant ou d’un point, pour spécifier l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ebeed-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="ebeed-111">La chaîne de nom de canal spécifiée par *PipeName* peut inclure n’importe quel caractère autre qu’une barre oblique inverse, y compris des chiffres et des caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="ebeed-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="ebeed-112">La chaîne du nom de canal entier peut comporter jusqu’à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="ebeed-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="ebeed-113">Les noms de canaux ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="ebeed-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="ebeed-114">Le serveur de canal ne peut pas créer un canal sur un autre ordinateur, donc [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) doit utiliser un point pour le nom du serveur, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="ebeed-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="ebeed-115">\\\\.\\ canal \\ *PipeName*</span><span class="sxs-lookup"><span data-stu-id="ebeed-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="ebeed-116">Un serveur de canaux peut fournir le nom du canal à ses clients de canal, afin qu’ils puissent se connecter au canal.</span><span class="sxs-lookup"><span data-stu-id="ebeed-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="ebeed-117">Le client de canal Découvre le nom du canal à partir d’une source persistante, telle qu’une entrée de Registre, un fichier ou une autre application.</span><span class="sxs-lookup"><span data-stu-id="ebeed-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="ebeed-118">Dans le cas contraire, les clients doivent connaître le nom du canal au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="ebeed-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
